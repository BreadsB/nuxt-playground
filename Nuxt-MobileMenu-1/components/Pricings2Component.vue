<template>
    <head>
        <meta charset="UTF-8">
        <title>Pricing Table</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet" >
        <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" >
        <link rel="stylesheet" href="style.css">
    </head>
    <section class="w-full min-h-screen py-36 bg-gray-100">
      <div class="container mx-auto px-4">
        <div class="flex flex-wrap -mx-10">
          <div v-for="(plan, index) in plans" :key="index" class="w-full sm:w-1/3 px-4 mb-8">
            <div :class="['card', `card-${index + 1}`]" class="relative max-w-sm mx-auto rounded-xl p-8 transition-transform duration-500 hover:scale-110">
              <div class="title text-center">
                <i :class="['fa', plan.icon]" class="text-white text-6xl w-24 h-24 rounded-full flex items-center justify-center mx-auto shadow-lg"></i>
                <h2 class="mt-5 text-2xl font-bold text-white">{{ plan.title }}</h2>
              </div>
              <div class="description text-center">
                <p class="text-lg text-white py-5 italic">{{ plan.description }}</p>
              </div>
              <div class="option">
                <ul class="text-white">
                  <li v-for="(feature, featureIndex) in plan.features" :key="featureIndex" class="mb-2">
                    <i :class="feature.available ? 'fa fa-check' : 'fa fa-times'" class="mr-2"></i>
                    {{ feature.text }}
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const plans = [
    {
      title: 'Basic',
      icon: 'fa-paper-plane',
      description: 'Perfect for anyone who what to show his presence in the Social Media',
      features: [
        { text: 'Publishing 4 posts per month', available: true },
        { text: 'Monthly basic report on performance', available: true },
        { text: 'Responding to messages and comments', available: true },
      ],
    },
    {
      title: 'Standard',
      icon: 'fa-plane',
      description: 'Ideal for fast growing Social Media',
      features: [
        { text: 'Publishing 8 posts per month (4+4 posts with personalised educational content)', available: true },
        { text: 'Responsing to messages and comments', available: true },
        { text: 'Monthly advanced report with performance analysis and recommendations', available: true },
        { text: 'Managing one paid advertising campaign on Meta Ads or Google Ads (e.g. promoting an event or searching new employee)', available: true },
      ],
    },
    {
      title: 'Premium',
      icon: 'fa-rocket',
      description: 'Advanced features for those who what best possible results',
      features: [
        { text: 'Publishing up to 12 posts per month (6+6 posts with personalised educational content)', available: true },
        { text: 'Responsing to messages and comments', available: true },
        { text: 'Monthly advanced report with performance analysis and recommendations', available: true },
        { text: 'Managing one paid advertising campaign on Meta Ads or Google Ads (e.g. promoting an event or searching new employee)', available: true },
        { text: 'Creation of 5 graphic content pieces (e.g., business cards, calendars) per month', available: true },
        { text: 'Generating ideas for organizing events and activities', available: true},
      ],
    },
  ];
  </script>
  
  <style scoped>
  .card {
    background: linear-gradient(-45deg, #fe0847, #feae3f);
  }
  
  .card-1 {
    background: linear-gradient(-45deg, #f403d1, #64b5f6);
  }
  
  .card-2 {
    background: linear-gradient(-45deg, #ffec61, #f321d7);
  }
  
  .card-3 {
    background: linear-gradient(-45deg, #24ff72, #9a4eff);
  }
  
  .card::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 40%;
    background: rgba(255, 255, 255, 0.1);
    z-index: 1;
    transform: skewY(-5deg) scale(1.5);
  }

  .title .fa{
  color:#fff;
  font-size: 60px;
  width: 100px;
  height: 100px;
  border-radius:  50%;
  text-align: center;
  line-height: 100px;
  -webkit-box-shadow: 0 10px 10px rgba(0,0,0,.1) ;
          box-shadow: 0 10px 10px rgba(0,0,0,.1) ;

}
  </style>