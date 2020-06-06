# Corona Blaster - Idea for the Moonshot Factory

<p align="center">
  <img src="/images/corona_blaster.gif">
</p>

## Introduction:
You’ve probably heard about [the bridge that collapsed back in 1831](http://scihi.org/broughton-suspension-bridge-resonance-disaster/) when an army brigade was marching across it. Or the opera singers (high C of a professional soprano?) shattering wine glasses with the power of their voice. These phenomena have one thing in common – resonant frequency.

Objects in our known world have natural vibration frequencies. By applying external force at the specific frequencies (mechanical, acoustic or electromagnetic) you can amplify the vibration. And with the higher intensify of the force this mechanical resonance may eventually break the object, thanks to some microscopic defects.

## Known resonant frequencies and the ways to induce them:
That is not a novelty though, as nowadays it’s quite a common procedure to [break the kidney stones with the ultrasound](https://www.nhs.uk/conditions/kidney-stones/treatment/). You can even buy a sound amplifier along with the compression driver from Amazon (all under £200), write a custom program on the computer (or an app for the smartphone) and shatter your old wine glasses from the comfort of your home (of course, with the permission of others 😊).

[Glass’ natural resonant frequency](https://sciencedemonstrations.fas.harvard.edu/presentations/shattering-wineglass) is at about 600 Hz, which is in the audible range and explains why it’s technically possible to break it with the high-intensity sound. But the same technique may also work with the microscopic objects like viruses!

A team from the Arizona State University was experimenting with [the satellite tobacco necrosis virus](https://www.researchgate.net/publication/5618885_Low_Frequency_Mechanical_Modes_of_Viral_Capsids_An_Atomistic_Approach) about 12 years ago and found that the virus was strongly resonating at the frequency of 60 Ghz. They used lasers at that time and still had to come up with an option of applying it to the viruses inside the human body.

As a relatively recent breakthrough, last year a team from the University of Nottingham produced an [acoustic laser](https://www.nottingham.ac.uk/news/using-sound-and-light-to-generate-ultra-fast-data-transfer) (they called it “saser”), which may generate sonic waves (phonons) in the THz range, penetrate tissue with a less absorption than a laser, but still without harmful ionisation specific to X-rays. So, it’s quite a promising technology for the medical screening and treatment (and beyond).

## Destructible structure of the virus:
To understand how we may destroy the virus, let’s look now at [its nature](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7138183/). Viruses contain their genetic code in DNA or RNA (latter is the case for COVID-19) protected by the protein shell (capsid). Genetic code of the viruses mutates, so the new strain of the virus may cause disease in the body that was resistant or immune to the earlier strain. That’s the reason of why we unfortunately still [didn’t eradicate the common flu virus](http://www.euro.who.int/en/health-topics/communicable-diseases/influenza/pandemic-influenza/how-pandemic-influenza-emerges) (which is, by the way, of RNA type as well) and thus seasonal vaccine has to be adjusted at least once a year. There are concerns that something similar may happen with the current coronavirus pandemic.

Details of the COVID-19’s protein structure can be found in the Research Collaboratory for Structural Bioinformatics (RCSB) [Protein Data Bank (PDB)](https://www.rcsb.org/). For this analysis I’ve looked particularly at 7BZ5 protein, which describes the structure of the virus’ crown-like receptor-binding spikes, giving the virus its specific shape and name – “coronavirus”.

To visualise it, you need to download [PDB file of 7BZ5](https://www.rcsb.org/structure/7BZ5) from the PDB Web site and open it with [PyMol](https://pymol.org/2/), a Python-based molecular visualisation tool, released as an open source and maintained by Schrödinger.

Then you can apply relevant filters to study more about the structure of the virus’s spike protein in detail, thanks to the chain data shared by the PDB microbiologists.
 
![7BZ5 visualisation in PyMol](/images/7BZ5_structure.jpg)

## Identifying virus protein shell’s resonant frequency:
Next step – is to get closer to identifying resonant frequencies of our target protein structure.

We can feed the same PDB file of 7BZ5 protein to the [chemical shift prediction Web service](http://spin.ccic.ohio-state.edu/index.php/ppm/document), built by the scientists of the Ohio State University. Powered by the GPU (graphics processing unit) processors, its backend uses linear and artificial neural network (ANN) algorithms, to predict chemical shift values for the protein structure of interest, separated by the amino acid residues.

As shown on the chart below, chemical shift values for the COVID-19’s protein spikes seem to be circa 4ppm (parts per million) for hydrogen, 32 ppm for carbon-beta, 63 ppm for carbon-alpha and 176 ppm for carbon atoms in the protein’s backbone.
 
![Chemical shift predictions for the virus’ spikes](/images/chem_shift.jpg)

Theoretically, using these PPM values (which represent frequency stability) and conducting experiments with the coronavirus samples and adjustable Terahertz generators, it may be possible to identify relevant resonant frequencies and prove if the virus spikes get damaged when the high-intensity energy is applied.

## Building handheld THz generators:
How feasible it’s to build a handheld, low-cost THz generator? Surprisingly, we are probably not that far from its realisation.

Use of THz generators is also of interest in the security space, thanks to its potential to identify weapons and explosives hidden under the person’s clothing. So, there were some funds allocated through the channels like Defence Advanced Research Projects Agency (DARPA) to develop new methods of the THz signals generation. And in June 2012 researchers from the Cornell University confirmed that they were able to [produce high-frequency signals using gallium nitride (GaN)](https://phys.org/news/2012-07-terahertz.html) chip.

In 2018 members of the Institute of Electrical and Electronics Engineers (IEEE), affiliated with the Massachusetts Institute of Technology (MIT), published results of their research where they were able to [generate high-power THz radiation using another semiconductor material, silicon-germanium (SiGe)](https://hangroup.mit.edu/wp-content/uploads/2018/04/2018_JSSC_1THz_Source.pdf).

In both cases we are talking about compact semiconductor chips, which may find their way even into the next generation of smartphones. This can make THz generators available and affordable to anyone in the world.

Use-case scenarios:
If practically proven and verified, this may dramatically change the course of actions in the fight against coronavirus.

 Just imagine at least one of these scenarios enabled:
-	Disinfection. From the personal protective equipment (PPE) to the cleaning of offices and public transport. Depending on the size of THz generator, it may be a cabinet where you put fabric for the anti-virus disinfection (so, that PPE can be re-used again) or a portable device that can be carried around to clean the target areas, e.g. your seat on the bus or an airplane;
-	Lung treatment: Chest-level machine which may be used to destroy virus colonies attached to the lung receptors;
-	Blood treatment: Kidney is another organ which may malfunction in the bodies of COVID-19 patients. Hospitals use special machines then to clean the blood (dialysis). Resonant frequency generator attached to such machine may be used to purify the blood additionally;
-	Anything else, which may help us to get back to the “normal ”life we had before this pandemic?
Can this be practically realised by any company or consortium, who have access to the relevant engineering, scientific and medical expertise. I hope so!
And I also hope that they can open source and release their solution(s) soon to save lives and support those in needs. Thank you!
