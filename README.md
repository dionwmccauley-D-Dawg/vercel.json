{
    "version": 2,
    "builds": [
        { "src": "index.html", "use": "@vercel/static" },
        { "src": "success.html", "use": "@vercel/static" },
        { "src": "cancel.html", "use": "@vercel/static" },
        { "src": "api/**/*.js", "use": "@vercel/node" }
    ],
    "routes": [
        { "src": "/api/(.*)", "dest": "/api/$1" },
        { "src": "/(.*)", "dest": "/$1" }
    ]
}
