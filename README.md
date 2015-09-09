# What is ionicResearchKit?

This is a clone of Apple's [ResearchKit Framework](https://github.com/ResearchKit/ResearchKit) built on [Ionic](https://github.com/driftyco/ionic) which makes it easy to create cross-platform hybrid native apps for medical research or for other research projects.

# Installation

1. Download and import the plugin script.<br />
`<script src="lib/ionic-researchkit/ionic-researchkit.js"></script>`
2. Download and import the plugin stylesheet.<br />
`<link href="lib/ionic-researchkit/ionic-researchkit.css" rel="stylesheet">`
3. Add `ionicResearchKit` to your angular app module dependencies list.<br />
`angular.module('myApp', ['ionicResearchKit']);`

# Usage

1. Add a modal view to your app using [$ionicModal](http://ionicframework.com/docs/api/service/$ionicModal/)
2. Add the following to your modal view template:

```
<ion-modal-view class="irk-modal">

  <irk-ordered-tasks>
	
    <irk-task>
    	<irk-instruction-step title="Your title here." text="Additional text can go here." />
  	</irk-task>

	  <irk-task>
    	<irk-scale-question-step id="data.q2" title="Your question here." text="Additional text can go here." 
    	    min="1" max="10" step="1" value="5" />
  	</irk-task>

  	<irk-task>
    	<irk-boolean-question-step id="data.q2" title="Your question here." text="Additional text can go here." 
    	    trueLabel="Yes" falseLabel="No"/>
	  </irk-task>

  </irk-ordered-tasks>

</ion-modal-view>
```

# Directives

`<irk-ordered-tasks>` is the equivalent of the `ORKOrderedTask` class in ResearchKit and will encompass one or more `<irk-task>` elements.

`<irk-task>` is the equivalent of the `ORKTask` class in ResearchKit and will encompass one of the available `<irk-*-step>` elements.

`<irk-instruction-step>` is the equivalent of the `ORKInstructionStep` class in ResearchKit and includes the `title` and `text` attributes.

`<irk-scale-question-step>` is the equivalent of the `ORKQuestionStep` and `ORKScaleAnswerFormat` classes in ResearchKit combined and includes the `id`, `title`, `text`, `min`, `max`, `step`, and `value` attributes.

`<irk-boolean-question-step>` is the equivalent of the `ORKQuestionStep` and `ORKBooleanAnswerFormat` classes in ResearchKit combined and includes the `id`, `title`, `text`, `trueLabel`, and `falseLabel` attributes.

*These are still a work in progress and I plan to have equivalent directives to all classes in ResearchKit.*

# Demo

![App demo](https://cloud.githubusercontent.com/assets/4361804/9769406/dff8d760-56de-11e5-9a08-b6d2f82ad894.gif)
