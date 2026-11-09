Cedric Jeng, cejeng@ucsd.edu
D42, Bijan Arbab

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic for us was how much the way data is recorded limits what you can conclude from it. Our project data has no field for a "misroute," so we had to work from imperfect signals such as referrals and returns to intake, and each one meant something different once we talked to City staff. We also saw that a status of "closed" can mean finished, referred out, or closed by an administrative step. This changed how we think about analysis, because choosing and defining the measure matters as much as the model.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

We want to test whether a report’s written description, used alongside its photo, predicts the correct category better than either alone. A photo can be ambiguous: a picture of a street could show a pothole, a sidewalk problem, or an illegally parked car. The description often adds the missing context, such as what the resident is reporting and where. We would compare an image-only model, a text-only model, and a combined model that uses both, using a vision-language model or fused image and text features. We would test each on a staff-labeled sample, to see whether the combination catches likely mismatches that a single input misses. A human reviewer would stay in the loop.

**3. What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**

We would define misroutes, and a way to measure them, at the start of the project, not near the end. Our work so far used proxies (referrals, “send back to intake,” reclassification) without a clear definition of an error or its cost, which limited what we could conclude. The City suggested a working rule: a case with three or more internal referrals counts as a misroute, with an exception for the Encampment category, which is routinely routed to several departments. Starting from a definition like that, we would work with staff to quantify the loss in labor, delay, and litigation risk, and design the analysis around it.

**4. What other techniques would you be interested in using in your project?**

- Image embeddings and clustering: Using a pretrained vision model to embed photos, then checking whether cases from different categories form separate groups, would show whether a photo-based check is feasible before building one.
- Zero-shot vision-language models: These could classify photos without training, which we could compare against a model trained on City data.
- Confidence calibration: We want a flag threshold that means something, such as "when the model says 80% unlikely, staff agree 80% of the time."
