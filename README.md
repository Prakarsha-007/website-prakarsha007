# website-prakarsha007
dark route hacathon
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Flood Management Dashboard</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>
</head>
<body class="bg-gradient-to-br from-blue-50 to-cyan-50 min-h-screen">
    <!-- Login Page -->
    <div id="loginPage" class="flex items-center justify-center min-h-screen bg-gradient-to-br from-blue-50 to-cyan-50">
        <div class="bg-white rounded-lg shadow-lg p-8 w-full max-w-md">
            <div class="text-center mb-6">
                <svg class="w-16 h-16 text-blue-600 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16V4m0 0L3 8m4-4l4 4m6 0v12m0 0l4-4m-4 4l-4-4"/>
                </svg>
                <h1 class="text-2xl font-bold text-gray-800">Smart Flood Management</h1>
                <p class="text-sm text-gray-600">Please log in to access the dashboard</p>
            </div>
            <form id="loginForm" onsubmit="handleLogin(event)">
                <div class="mb-4">
                    <label for="username" class="block text-sm font-medium text-gray-700">Username</label>
                    <input type="text" id="username" name="username" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>
                <div class="mb-6">
                    <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
                    <input type="password" id="password" name="password" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>
                <button type="submit" class="w-full bg-blue-600 text-white py-2 px-4 rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">Log In</button>
            </form>
            <p id="loginError" class="mt-4 text-sm text-red-600 text-center hidden">Invalid username or password.</p>
        </div>
    </div>

    <!-- Dashboard (hidden initially) -->
    <div id="dashboard" class="hidden">
        <header class="bg-white shadow-md border-b-4 border-blue-600">
            <div class="max-w-7xl mx-auto px-6 py-4">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <svg class="w-10 h-10 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16V4m0 0L3 8m4-4l4 4m6 0v12m0 0l4-4m-4 4l-4-4"/>
                        </svg>
                        <div>
                            <h1 class="text-2xl font-bold text-gray-800">Smart Flood Management System</h1>
                            <p class="text-sm text-gray-600">Real-Time Monitoring & Control</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <div class="flex items-center gap-2">
                            <span class="text-sm font-medium text-gray-700">Auto Mode</span>
                            <button onclick="toggleAutoMode()" id="autoModeBtn" class="w-12 h-6 rounded-full bg-blue-600 relative transition-colors">
                                <div id="autoModeToggle" class="w-5 h-5 bg-white rounded-full shadow absolute top-0.5 left-6 transition-transform"></div>
                            </button>
                        </div>
                        <svg class="w-6 h-6 text-gray-600 cursor-pointer hover:text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"/>
                        </svg>
                    </div>
                </div>
            </div>
        </header>

        <div class="bg-white shadow-sm border-b">
            <div class="max-w-7xl mx-auto px-6">
                <div class="flex gap-6">
                    <button onclick="switchTab('overview')" class="tab-btn py-3 px-4 font-medium border-b-2 border-blue-600 text-blue-600">Overview</button>
                    <button onclick="switchTab('zones')" class="tab-btn py-3 px-4 font-medium border-b-2 border-transparent text-gray-600 hover:text-blue-600">Zones</button>
              ...
