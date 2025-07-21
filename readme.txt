

           ▄▄▄▄▄▄▄ ▄▄▄▄▄▀▀▀▀▀▄       
        ▄▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▄      
     ▄▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀     
    ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▄     
    ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀    
   ▄▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▄   
 ▄▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀  
▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 
 ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀
   ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀
  ▀▀▀▀▀▀▀▀ ▀ ▀▀▀ ▀▀ ▀▀▀▀▀▀▀▀▄ ▀▀▀▀▀▀ 
   ▀▀▀▀▀▀           ▀▀▀▀▀▀▀▀▀        
                     ▀▀▀▀▀▀          
 

    <!-- Page 3: Generate Color Palette -->
    <div id="page3" class="page pt-20">
        <div class="container mx-auto px-4 py-10">
            <h2 class="text-3xl font-bold text-center text-white mb-10">Generate Color Palette</h2>
            
            <div class="max-w-4xl mx-auto">
                <div class="bg-white rounded-xl shadow-md p-6 mb-8">
                    <div class="flex flex-col md:flex-row gap-8">
                        <div class="md:w-1/2">
                            <div class="flex justify-center mb-6">
                                <img id="generatedImage" class="w-full rounded-lg" src="" alt="Image being analyzed for color palette"/>
                            </div>
                            <div class="flex justify-center gap-4">
                                <button id="generatePaletteBtn" class="generate-btn text-white px-6 py-2 rounded-md text-sm font-medium">Generate Palette</button>
                                <button onclick="document.getElementById('imageUpload').click()" class="border border-gray-300 px-6 py-2 rounded-md text-sm font-medium">Change Image</button>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2">
                            <h3 class="text-lg font-medium text-gray-700 mb-4">Color Extraction Options</h3>
                            
                            <div class="space-y-4 mb-6">
                                <div>
                                    <label for="colorCount" class="block text-sm font-medium text-gray-700 mb-1">Number of Colors</label>
                                    <select id="colorCount" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                        <option value="5">5</option>
                                        <option value="8" selected>8</option>
                                        <option value="12">12</option>
                                        <option value="16">16</option>
                                    </select>
                                </div>
                                
                                <div>
                                    <label for="algorithmType" class="block text-sm font-medium text-gray-700 mb-1">Algorithm</label>
                                    <select id="algorithmType" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                        <option value="kmeans">K-Means Clustering</option>
                                    </select>
                                </div>
                            </div>
                            
                            <div id="palettePreview" class="hidden">
                                <h3 class="text-lg font-medium text-gray-700 mb-4">Generated Palette Preview</h3>
                                <div class="flex flex-wrap gap-2 mb-4" id="paletteColorsContainer">
                                    <!-- Palette preview will be generated here -->
                                </div>
                                <button onclick="showPage('page4')" class="generate-btn text-white px-6 py-2 rounded-md text-sm font-medium">View Detailed Palette</button>
                            </div>
                            
                            <div id="loadingIndicator" class="hidden">
                                <div class="loading-spinner"></div>
                                <p class="text-center text-gray-600">Analyzing image colors...</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    7