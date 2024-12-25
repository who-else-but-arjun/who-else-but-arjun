import React from 'react';
import { Activity, Brain, BookOpen, Users, Github, Linkedin, Mail } from 'lucide-react';
import { Card, CardContent } from '@/components/ui/card';

const GithubProfile = () => {
  const skills = {
    'Deep Learning': 90,
    'CNN': 85,
    'RNN': 75,
    'NLP': 70,
    'Data Analytics': 80,
    'Generative AI': 65
  };

  return (
    <div className="max-w-4xl mx-auto p-6 space-y-6">
      {/* Header Section */}
      <div className="text-center space-y-4">
        <h1 className="text-4xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
          Hi 👋, I'm Arjun
        </h1>
        <p className="text-xl text-gray-600">
          AI/ML Engineer | Deep Learning Enthusiast
        </p>
      </div>
      <Card className="hover:shadow-lg transition-shadow duration-300">
        <CardContent className="p-6">
          <div className="flex items-center space-x-2 mb-4">
            <Brain className="w-6 h-6 text-blue-600" />
            <h2 className="text-2xl font-semibold">About Me</h2>
          </div>
          <div className="space-y-3">
            <div className="flex items-start space-x-2">
              <Activity className="w-5 h-5 mt-1 text-gray-600" />
              <p>Passionate about convolutional neural networks (CNNs), machine learning (ML), neural networks (NN), and data analytics</p>
            </div>
            <div className="flex items-start space-x-2">
              <BookOpen className="w-5 h-5 mt-1 text-gray-600" />
              <p>Currently learning recurrent neural networks (RNNs), natural language processing (NLP), and generative AI</p>
            </div>
            <div className="flex items-start space-x-2">
              <Users className="w-5 h-5 mt-1 text-gray-600" />
              <p>Looking to collaborate on projects involving deep learning, data-driven insights, and generative models</p>
            </div>
          </div>
        </CardContent>
      </Card>
      <Card className="hover:shadow-lg transition-shadow duration-300">
        <CardContent className="p-6">
          <h2 className="text-2xl font-semibold mb-4">Skills</h2>
          <div className="space-y-4">
            {Object.entries(skills).map(([skill, level]) => (
              <div key={skill} className="space-y-2">
                <div className="flex justify-between">
                  <span className="font-medium">{skill}</span>
                  <span className="text-gray-600">{level}%</span>
                </div>
                <div className="h-2 bg-gray-200 rounded-full">
                  <div
                    className="h-full bg-gradient-to-r from-blue-600 to-purple-600 rounded-full transition-all duration-500"
                    style={{ width: `${level}%` }}
                  />
                </div>
              </div>
            ))}
          </div>
        </CardContent>
      </Card>
      <div className="flex justify-center space-x-4">
        <a href="#" className="p-2 rounded-full hover:bg-gray-100 transition-colors duration-300">
          <Github className="w-6 h-6" />
        </a>
        <a href="#" className="p-2 rounded-full hover:bg-gray-100 transition-colors duration-300">
          <Linkedin className="w-6 h-6 text-blue-600" />
        </a>
        <a href="#" className="p-2 rounded-full hover:bg-gray-100 transition-colors duration-300">
          <Mail className="w-6 h-6 text-red-500" />
        </a>
      </div>
    </div>
  );
};

export default GithubProfile;
