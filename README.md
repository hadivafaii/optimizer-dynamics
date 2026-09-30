# Optimizer Dynamics Lab

[Open the playground](https://hadivafaii.github.io/optimizer-dynamics/) ·
[Try an embedded landscape](https://hadivafaii.github.io/optimizer-dynamics/?embed=1&scene=curved-valley)

Explore how optimizers move through curved valleys, sharp ravines, and noisy
landscapes. Saved examples play immediately, with controls for playback, 2D/3D,
and optimizer visibility. The same renderer supports compact blog embeds.

All trajectories are computed by the actual Python/PyTorch implementations in
[massive-lion](https://github.com/hadivafaii/massive-lion/tree/codex/hosted-dynamics-lab).
This repository contains deployment configuration and frozen published figures;
it does not maintain a second implementation of the optimizers.

## Enable custom runs

The public site starts with instant saved examples. To enable arbitrary new
settings, deploy the prepared free Python backend:

[Deploy the free backend to Render](https://render.com/deploy?repo=https%3A%2F%2Fgithub.com%2Fhadivafaii%2Fmassive-lion%2Ftree%2Fcodex%2Fhosted-dynamics-lab)

Sign up, review the **Free** plan, and deploy. Send the resulting service URL
back to Codex to finish connecting it, or set repository Actions variable
`DYNAMICS_API_URL` to the `https://…onrender.com` origin and rerun **Publish
playground**. No `/api` suffix is needed. Free servers can take about a minute
to wake; saved figures keep working while the server is asleep.

## Publish a blog figure

Choose a saved scene and click **Embed** to copy its iframe. For a custom
experiment, complete its run and use **Download scene**. Give the bundle a
unique `id` such as `article-valley-v1`, save it under `published/`, and push.
The build copies that exact snapshot without rerunning it. It appears in the
scene picker and is available at `?embed=1&scene=article-valley-v1`.

Keep published ids and files unchanged. Use a new id for a revised figure.
Each bundle records configuration and source provenance. Built-in demos are
generated from the source revision pinned in `.github/workflows/pages.yml`;
change that revision deliberately when updating the application.

[Full hosting and local preview guide](https://github.com/hadivafaii/massive-lion/blob/codex/hosted-dynamics-lab/docs/dynamics_lab_hosting.md)
