# The Annotated Diffusion Model
In this blog post, we'll take a deeper look into Denoising Diffusion Probabilistic Models (also known as DDPMs, diffusion models, score-based generative models or simply autoencoders) as researchers have been able to achieve remarkable results with them for (un)conditional image/audio/video generation. Popular examples (at the time of writing) include GLIDE and DALL-E 2 by OpenAI, Latent Diffusion by the University of Heidelberg and ImageGen by Google Brain.
We'll go over the original DDPM paper by (Ho et al., 2020), implementing it step-by-step in PyTorch, based on Phil Wang's implementation - which itself is based on the original TensorFlow implementation. Note that the idea of diffusion for generative modeling was actually already introduced in (Sohl-Dickstein et al., 2015). However, it took until (Song et al., 2019) (at Stanford University), and then (Ho et al., 2020) (at Google Brain) who independently improved the approach.

Note that there are several perspectives on diffusion models. Here, we employ the discrete-time (latent variable model) perspective, but be sure to check out the other perspectives as well.

Alright, let's dive in!
