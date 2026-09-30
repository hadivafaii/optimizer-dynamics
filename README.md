# Optimizer Dynamics Lab

[Open the playground](https://hadivafaii.github.io/optimizer-dynamics/) ·
[Try an embedded landscape](https://hadivafaii.github.io/optimizer-dynamics/?embed=1&scene=curved-valley)

Explore how optimizers move through curved valleys, sharp ravines, and noisy
landscapes. Saved examples play immediately, with controls for playback, 2D/3D,
and optimizer visibility. The same renderer supports compact blog embeds.

All trajectories are computed by the actual Python/PyTorch implementations in
[massive-lion](https://github.com/hadivafaii/massive-lion/tree/main).
This repository contains deployment configuration and frozen published figures;
it does not maintain a second implementation of the optimizers.

## Custom runs

Saved examples play immediately. Custom settings run through the free
[Python backend](https://optimizer-dynamics-api.onrender.com/api/health), which
uses the optimizer code on `massive-lion/main`. Free servers can take about a
minute to wake; saved figures keep working while the server is asleep.

To deploy your own copy, [deploy the free backend to Render](https://render.com/deploy?repo=https%3A%2F%2Fgithub.com%2Fhadivafaii%2Fmassive-lion%2Ftree%2Fmain).

Review the **Free** plan and deploy. Set repository Actions variable
`DYNAMICS_API_URL` to the `https://…onrender.com` origin and rerun **Publish
playground**. No `/api` suffix is needed.

## Publish a blog figure

Choose a saved scene and click **Embed** to copy its iframe. For a custom
experiment, complete its run and use **Download scene**. Give the bundle a
unique `id` such as `article-valley-v1`, save it under `published/`, and push.
The build copies that exact snapshot without rerunning it. It appears in the
scene picker and is available at `?embed=1&scene=article-valley-v1`.

Keep published ids and files unchanged. Use a new id for a revised figure.
Each bundle records configuration and source provenance. Built-in demos are
generated from `massive-lion/main`. After source updates, deploy the latest
commit in Render and run **Publish playground** here to refresh the application.
Each build records the exact source commit in its provenance.

[Full hosting and local preview guide](https://github.com/hadivafaii/massive-lion/blob/main/docs/dynamics_lab_hosting.md)
