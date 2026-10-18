<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Autosurveillance STEP - Saisie Terrain (Laurent Juillien)</title>
  
  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            step: {
              50: '#f0f9ff',
              100: '#e0f2fe',
              500: '#0284c7',
              600: '#0369a1',
              700: '#0f4c81',
              800: '#075985',
              900: '#0c4a6e',
            }
          }
        }
      }
    }
  </script>

  <!-- jsPDF via CDN -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    body {
      font-family: 'Plus Jakarta Sans', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      -webkit-tap-highlight-color: transparent;
    }
    .font-mono-numbers {
      font-family: 'JetBrains Mono', monospace;
    }
    input[type="number"]::-webkit-inner-spin-button,
    input[type="number"]::-webkit-outer-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }
  </style>
</head>
<body class="bg-slate-100 text-slate-800 min-h-screen flex flex-col antialiased selection:bg-sky-200">

  <!-- En-tête de navigation -->
  <header class="bg-slate-900 text-white shadow-md border-b border-slate-800 sticky top-0 z-30">
    <div class="max-w-4xl mx-auto px-4 py-3 flex items-center justify-between">
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-sky-600 to-cyan-400 flex items-center justify-center text-white shadow-lg shadow-sky-950/40">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z" />
          </svg>
        </div>
        <div>
          <h1 class="text-base sm:text-lg font-bold leading-tight tracking-tight text-white flex items-center gap-2">
            Autosurveillance STEP
            <span class="text-xs px-2 py-0.5 rounded-full bg-sky-900/80 text-sky-300 font-mono border border-sky-700/60 font-medium">Terrain 24h</span>
          </h1>
          <p class="text-xs text-slate-400">Station d'Épuration • Bilan Réglementaire Terrain</p>
        </div>
      </div>

      <div class="flex items-center gap-2">
        <div class="hidden sm:flex items-center gap-1.5 bg-slate-800 px-2.5 py-1.5 rounded-lg border border-slate-700 text-xs text-slate-300">
          <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
          <span class="text-emerald-400 font-semibold">Partage: WhatsApp &amp; Mail</span>
        </div>
        <button id="btnExemple" type="button" class="text-xs bg-slate-800 hover:bg-slate-700 active:bg-slate-600 text-slate-200 px-3 py-2 rounded-lg font-medium transition border border-slate-700 flex items-center gap-1.5 shadow-sm cursor-pointer">
          <svg class="w-3.5 h-3.5 text-amber-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
          </svg>
          <span class="hidden sm:inline">Exemple</span>
        </button>
        <button id="btnReset" type="button" class="text-xs text-rose-300 hover:text-rose-200 bg-rose-950/40 hover:bg-rose-900/50 px-2.5 py-2 rounded-lg border border-rose-800/60 transition cursor-pointer" title="Effacer tout">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
          </svg>
        </button>
      </div>
    </div>
  </header>

  <!-- Contenu Principal -->
  <main class="max-w-4xl mx-auto w-full px-3 sm:px-6 py-6 flex-1 space-y-6">

    <!-- Formulaire Principal -->
    <form id="stepForm" class="space-y-6" novalidate>

      <!-- 1. Informations Générales -->
      <section class="bg-white rounded-2xl p-4 sm:p-6 shadow-sm border border-slate-200">
        <div class="flex items-center gap-2.5 pb-3 mb-4 border-b border-slate-100">
          <div class="w-7 h-7 rounded-lg bg-sky-100 text-sky-700 flex items-center justify-center font-bold text-sm">
            1
          </div>
          <h2 class="text-base sm:text-lg font-bold text-slate-900">
            En-tête &amp; Informations Générales
          </h2>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <!-- Nom de la STEP -->
          <div>
            <label for="nomStep" class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1.5">
              Nom de la Station d'Épuration (STEP) <span class="text-rose-500">*</span>
            </label>
            <input
              type="text"
              id="nomStep"
              name="nomStep"
              placeholder="ex: STEP du Val d'Allier (50 000 EH)"
              class="w-full px-4 py-3 text-base rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 focus:border-sky-500 bg-slate-50/50 transition"
              required
            >
            <p id="err-nomStep" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
          </div>

          <!-- Date de l'autosurveillance -->
          <div>
            <label for="dateAutosurveillance" class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1.5">
              Date de l'autosurveillance <span class="text-rose-500">*</span>
            </label>
            <input
              type="date"
              id="dateAutosurveillance"
              name="dateAutosurveillance"
              class="w-full px-4 py-3 text-base rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 focus:border-sky-500 bg-slate-50/50 transition"
              required
            >
            <p id="err-dateAutosurveillance" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
          </div>

          <!-- Technicien / Opérateur -->
          <div>
            <label for="technicienNom" class="block text-xs font-semibold text-slate-600 mb-1.5">
              Technicien / Opérateur de traitement <span class="text-slate-400">(optionnel)</span>
            </label>
            <input
              type="text"
              id="technicienNom"
              name="technicienNom"
              placeholder="ex: Laurent Juillien"
              class="w-full px-3.5 py-2.5 text-sm rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-sky-500 bg-slate-50/30"
            >
          </div>

          <!-- Conditions Météo -->
          <div>
            <label for="meteo" class="block text-xs font-semibold text-slate-600 mb-1.5">
              Conditions Météorologiques <span class="text-slate-400">(optionnel)</span>
            </label>
            <select
              id="meteo"
              name="meteo"
              class="w-full px-3.5 py-2.5 text-sm rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-sky-500 bg-slate-50/30"
            >
              <option value="Temps sec">Temps sec</option>
              <option value="Pluie modérée">Pluie modérée</option>
              <option value="Forte pluie / Orage">Forte pluie / Orage</option>
              <option value="Gel / Neige">Gel / Neige</option>
              <option value="Vent fort">Vent fort</option>
            </select>
          </div>
        </div>
      </section>

      <!-- Grille des Prélèvements 24H (Entrée et Sortie) -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

        <!-- 2. BILAN ENTRÉE -->
        <section class="bg-white rounded-2xl p-4 sm:p-5 shadow-sm border-2 border-sky-200 flex flex-col justify-between">
          <div>
            <div class="flex items-center justify-between pb-3 mb-4 border-b border-sky-100">
              <div class="flex items-center gap-2">
                <div class="w-7 h-7 rounded-lg bg-sky-600 text-white flex items-center justify-center font-bold text-sm">
                  2
                </div>
                <div>
                  <h2 class="text-base font-bold text-sky-950">Bilan Entrée</h2>
                  <p class="text-xs text-sky-700">Prélèvement Eaux Brutes</p>
                </div>
              </div>
              <span class="text-[10px] font-bold px-2 py-1 rounded bg-sky-100 text-sky-800 border border-sky-200 uppercase">
                Préleveur Entrée
              </span>
            </div>

            <div class="space-y-4">
              <div class="grid grid-cols-2 gap-3">
                <!-- Date prélèvement -->
                <div>
                  <label for="entreeDate" class="block text-xs font-semibold text-slate-700 mb-1">
                    Date prélèvement <span class="text-rose-500">*</span>
                  </label>
                  <input
                    type="date"
                    id="entreeDate"
                    name="entreeDate"
                    class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 bg-slate-50/50"
                    required
                  >
                  <p id="err-entreeDate" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
                </div>

                <!-- Heure relève -->
                <div>
                  <label for="entreeHeure" class="block text-xs font-semibold text-slate-700 mb-1">
                    Heure relève <span class="text-rose-500">*</span>
                  </label>
                  <input
                    type="time"
                    id="entreeHeure"
                    name="entreeHeure"
                    class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 bg-slate-50/50"
                    required
                  >
                  <p id="err-entreeHeure" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
                </div>
              </div>

              <!-- Température au niveau du préleveur -->
              <div>
                <label for="entreeTemperature" class="block text-xs font-semibold text-slate-700 mb-1 flex items-center justify-between">
                  <span>Température préleveur (°C) <span class="text-rose-500">*</span></span>
                  <span class="text-[11px] text-slate-400 font-normal">Norme : 2°C à 5°C</span>
                </label>
                <div class="relative">
                  <input
                    type="number"
                    step="0.1"
                    id="entreeTemperature"
                    name="entreeTemperature"
                    placeholder="ex: 3.4"
                    class="w-full pl-3.5 pr-12 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 font-mono-numbers bg-slate-50/50"
                    required
                  >
                  <span class="absolute right-3.5 top-2.5 text-xs font-bold text-slate-400">°C</span>
                </div>
                <p id="err-entreeTemperature" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

              <!-- Débit écoulé sur 24 heures -->
              <div>
                <label for="entreeDebit" class="block text-xs font-semibold text-slate-700 mb-1">
                  Débit écoulé sur 24h (m³) <span class="text-rose-500">*</span>
                </label>
                <div class="relative">
                  <input
                    type="number"
                    step="0.1"
                    min="0"
                    id="entreeDebit"
                    name="entreeDebit"
                    placeholder="ex: 1845.2"
                    class="w-full pl-3.5 pr-12 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-sky-500 font-mono-numbers bg-slate-50/50"
                    required
                  >
                  <span class="absolute right-3.5 top-2.5 text-xs font-bold text-slate-400">m³</span>
                </div>
                <p id="err-entreeDebit" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

              <!-- Capture Photo Entrée avec caméra arrière forcée (capture="environment") -->
              <div class="pt-2">
                <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1.5 flex items-center justify-between">
                  <span>Photo Préleveur Entrée <span class="text-rose-500">*</span></span>
                  <span class="text-[11px] text-sky-600 font-medium">Caméra arrière directe</span>
                </label>

                <!-- Input File avec attributs obligatoires -->
                <input
                  type="file"
                  id="entreePhotoInput"
                  accept="image/*"
                  capture="environment"
                  class="hidden"
                >

                <!-- Zone d'affichage / déclenchement -->
                <div id="entreePhotoBox" class="border-2 border-dashed border-sky-300 bg-sky-50/60 rounded-xl p-3 text-center cursor-pointer hover:bg-sky-100/60 active:scale-[0.99] transition relative overflow-hidden min-h-[140px] flex flex-col items-center justify-center">
                  <div id="entreePlaceholder" class="space-y-2">
                    <div class="w-12 h-12 mx-auto rounded-full bg-sky-200/80 text-sky-700 flex items-center justify-center">
                      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 9a2 2 0 012-2h.93a2 2 0 001.664-.89l.812-1.22A2 2 0 0110.07 4h3.86a2 2 0 011.664.89l.812 1.22A2 2 0 0018.07 7H19a2 2 0 012 2v9a2 2 0 01-2 2H5a2 2 0 01-2-2V9z"/>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13a3 3 0 11-6 0 3 3 0 016 0z"/>
                      </svg>
                    </div>
                    <p class="text-xs font-bold text-sky-900">Prendre photo Entrée</p>
                    <p class="text-[11px] text-slate-500">Ouvre directement la caméra arrière</p>
                  </div>

                  <!-- Aperçu miniature -->
                  <div id="entreePreviewContainer" class="hidden w-full h-full flex flex-col items-center">
                    <img id="entreePreviewImg" src="" alt="Aperçu Entrée" class="w-full h-36 object-cover rounded-lg shadow-sm border border-slate-200">
                    <div class="mt-2 flex items-center gap-2">
                      <button type="button" id="btnChangeEntreePhoto" class="text-xs px-2.5 py-1 bg-white border border-slate-300 rounded shadow-sm text-slate-700 hover:bg-slate-50 font-medium">
                        Reprendre
                      </button>
                      <button type="button" id="btnDeleteEntreePhoto" class="text-xs px-2.5 py-1 bg-rose-50 border border-rose-200 rounded shadow-sm text-rose-600 hover:bg-rose-100 font-medium">
                        Supprimer
                      </button>
                    </div>
                  </div>
                </div>
                <p id="err-entreePhoto" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

            </div>
          </div>
        </section>

        <!-- 3. BILAN SORTIE -->
        <section class="bg-white rounded-2xl p-4 sm:p-5 shadow-sm border-2 border-emerald-200 flex flex-col justify-between">
          <div>
            <div class="flex items-center justify-between pb-3 mb-4 border-b border-emerald-100">
              <div class="flex items-center gap-2">
                <div class="w-7 h-7 rounded-lg bg-emerald-600 text-white flex items-center justify-center font-bold text-sm">
                  3
                </div>
                <div>
                  <h2 class="text-base font-bold text-emerald-950">Bilan Sortie</h2>
                  <p class="text-xs text-emerald-700">Prélèvement Eaux Traitées / Rejet</p>
                </div>
              </div>
              <span class="text-[10px] font-bold px-2 py-1 rounded bg-emerald-100 text-emerald-800 border border-emerald-200 uppercase">
                Préleveur Sortie
              </span>
            </div>

            <div class="space-y-4">
              <div class="grid grid-cols-2 gap-3">
                <!-- Date prélèvement -->
                <div>
                  <label for="sortieDate" class="block text-xs font-semibold text-slate-700 mb-1">
                    Date prélèvement <span class="text-rose-500">*</span>
                  </label>
                  <input
                    type="date"
                    id="sortieDate"
                    name="sortieDate"
                    class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-emerald-500 bg-slate-50/50"
                    required
                  >
                  <p id="err-sortieDate" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
                </div>

                <!-- Heure relève -->
                <div>
                  <label for="sortieHeure" class="block text-xs font-semibold text-slate-700 mb-1">
                    Heure relève <span class="text-rose-500">*</span>
                  </label>
                  <input
                    type="time"
                    id="sortieHeure"
                    name="sortieHeure"
                    class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-emerald-500 bg-slate-50/50"
                    required
                  >
                  <p id="err-sortieHeure" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
                </div>
              </div>

              <!-- Température au niveau du préleveur -->
              <div>
                <label for="sortieTemperature" class="block text-xs font-semibold text-slate-700 mb-1 flex items-center justify-between">
                  <span>Température préleveur (°C) <span class="text-rose-500">*</span></span>
                  <span class="text-[11px] text-slate-400 font-normal">Norme : 2°C à 5°C</span>
                </label>
                <div class="relative">
                  <input
                    type="number"
                    step="0.1"
                    id="sortieTemperature"
                    name="sortieTemperature"
                    placeholder="ex: 3.8"
                    class="w-full pl-3.5 pr-12 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-emerald-500 font-mono-numbers bg-slate-50/50"
                    required
                  >
                  <span class="absolute right-3.5 top-2.5 text-xs font-bold text-slate-400">°C</span>
                </div>
                <p id="err-sortieTemperature" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

              <!-- Débit écoulé sur 24 heures -->
              <div>
                <label for="sortieDebit" class="block text-xs font-semibold text-slate-700 mb-1">
                  Débit écoulé sur 24h (m³) <span class="text-rose-500">*</span>
                </label>
                <div class="relative">
                  <input
                    type="number"
                    step="0.1"
                    min="0"
                    id="sortieDebit"
                    name="sortieDebit"
                    placeholder="ex: 1812.0"
                    class="w-full pl-3.5 pr-12 py-2.5 text-sm rounded-xl border border-slate-300 focus:outline-none focus:ring-2 focus:ring-emerald-500 font-mono-numbers bg-slate-50/50"
                    required
                  >
                  <span class="absolute right-3.5 top-2.5 text-xs font-bold text-slate-400">m³</span>
                </div>
                <p id="err-sortieDebit" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

              <!-- Capture Photo Sortie avec caméra arrière forcée (capture="environment") -->
              <div class="pt-2">
                <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1.5 flex items-center justify-between">
                  <span>Photo Préleveur Sortie <span class="text-rose-500">*</span></span>
                  <span class="text-[11px] text-emerald-600 font-medium">Caméra arrière directe</span>
                </label>

                <!-- Input File avec attributs obligatoires -->
                <input
                  type="file"
                  id="sortiePhotoInput"
                  accept="image/*"
                  capture="environment"
                  class="hidden"
                >

                <div id="sortiePhotoBox" class="border-2 border-dashed border-emerald-300 bg-emerald-50/60 rounded-xl p-3 text-center cursor-pointer hover:bg-emerald-100/60 active:scale-[0.99] transition relative overflow-hidden min-h-[140px] flex flex-col items-center justify-center">
                  <div id="sortiePlaceholder" class="space-y-2">
                    <div class="w-12 h-12 mx-auto rounded-full bg-emerald-200/80 text-emerald-700 flex items-center justify-center">
                      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 9a2 2 0 012-2h.93a2 2 0 001.664-.89l.812-1.22A2 2 0 0110.07 4h3.86a2 2 0 011.664.89l.812 1.22A2 2 0 0018.07 7H19a2 2 0 012 2v9a2 2 0 01-2 2H5a2 2 0 01-2-2V9z"/>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13a3 3 0 11-6 0 3 3 0 016 0z"/>
                      </svg>
                    </div>
                    <p class="text-xs font-bold text-emerald-950">Prendre photo Sortie</p>
                    <p class="text-[11px] text-slate-500">Ouvre directement la caméra arrière</p>
                  </div>

                  <div id="sortiePreviewContainer" class="hidden w-full h-full flex flex-col items-center">
                    <img id="sortiePreviewImg" src="" alt="Aperçu Sortie" class="w-full h-36 object-cover rounded-lg shadow-sm border border-slate-200">
                    <div class="mt-2 flex items-center gap-2">
                      <button type="button" id="btnChangeSortiePhoto" class="text-xs px-2.5 py-1 bg-white border border-slate-300 rounded shadow-sm text-slate-700 hover:bg-slate-50 font-medium">
                        Reprendre
                      </button>
                      <button type="button" id="btnDeleteSortiePhoto" class="text-xs px-2.5 py-1 bg-rose-50 border border-rose-200 rounded shadow-sm text-rose-600 hover:bg-rose-100 font-medium">
                        Supprimer
                      </button>
                    </div>
                  </div>
                </div>
                <p id="err-sortiePhoto" class="text-xs text-rose-500 font-medium mt-1 hidden"></p>
              </div>

            </div>
          </div>
        </section>

      </div>

      <!-- Observations complémentaires -->
      <section class="bg-white rounded-2xl p-4 sm:p-5 shadow-sm border border-slate-200">
        <label for="observations" class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1.5 flex items-center justify-between">
          <span>Remarques / Événements d'exploitation <span class="text-slate-400 font-normal">(optionnel)</span></span>
          <span class="text-[11px] text-slate-400">ex: Nettoyage dégrilleur, incident, surverse...</span>
        </label>
        <textarea
          id="observations"
          name="observations"
          rows="2"
          placeholder="Renseignez ici d'éventuelles observations (couleur de l'effluent, état des flacons, entretien préleveur, absence de pluie...)"
          class="w-full px-3.5 py-2.5 text-sm rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-sky-500 resize-none bg-slate-50/30"
        ></textarea>
      </section>

      <!-- 4. GÉNÉRATION DU RAPPORT PDF & OPTIONS DE PARTAGE -->
      <section class="bg-gradient-to-br from-slate-900 to-slate-800 text-white rounded-2xl p-5 sm:p-6 shadow-xl border border-slate-700">
        <div class="flex items-center gap-2.5 pb-3 mb-4 border-b border-slate-700">
          <div class="w-7 h-7 rounded-lg bg-emerald-500 text-white flex items-center justify-center font-bold text-sm">
            4
          </div>
          <div>
            <h2 class="text-base sm:text-lg font-bold text-white">
              Génération du Rapport PDF &amp; Options de Partage
            </h2>
            <p class="text-xs text-slate-300">
              Génération instantanée du rapport officiel avec photos horodatées, prêt pour envoi direct par WhatsApp ou par e-mail
            </p>
          </div>
        </div>

        <div class="space-y-4">
          <!-- Carte des options de partage direct -->
          <div class="p-4 rounded-xl bg-slate-800/90 border border-slate-700 space-y-3">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
              <div class="flex items-start gap-3 p-3 rounded-xl bg-slate-900/60 border border-slate-700/60">
                <div class="w-9 h-9 rounded-lg bg-[#25D366]/20 text-[#25D366] flex items-center justify-center shrink-0">
                  <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                    <path d="M12.04 2c-5.46 0-9.91 4.45-9.91 9.91 0 1.75.46 3.45 1.32 4.95L2.05 22l5.25-1.38c1.45.79 3.08 1.21 4.74 1.21 5.46 0 9.91-4.45 9.91-9.91 0-2.65-1.03-5.14-2.9-7.01A9.816 9.816 0 0012.04 2zm.01 1.67c4.54 0 8.24 3.7 8.24 8.24 0 2.2-.86 4.27-2.42 5.82-1.55 1.56-3.62 2.42-5.82 2.42-1.48 0-2.93-.39-4.21-1.15l-.3-.18-3.12.82.83-3.04-.2-.31c-.83-1.32-1.27-2.86-1.27-4.38 0-4.54 3.7-8.24 8.24-8.24zm-3.62 4.75c-.2 0-.44.08-.66.32-.22.24-.86.84-.86 2.05s.88 2.38 1 2.55c.12.16 1.7 2.6 4.13 3.65.58.25 1.03.4 1.38.51.58.19 1.11.16 1.53.1.47-.07 1.44-.59 1.64-1.15.2-.57.2-1.05.14-1.15-.06-.1-.22-.16-.46-.28-.24-.12-1.44-.71-1.66-.79-.22-.08-.38-.12-.54.12-.16.24-.62.79-.76.95-.14.16-.28.18-.52.06-.24-.12-1.01-.37-1.92-1.19-.71-.63-1.19-1.41-1.33-1.65-.14-.24-.01-.37.11-.49.11-.11.24-.28.36-.42.12-.14.16-.24.24-.4.08-.16.04-.3-.02-.42-.06-.12-.54-1.3-.74-1.78-.19-.48-.39-.41-.54-.42h-.47z"/>
                  </svg>
                </div>
                <div>
                  <h4 class="text-xs font-bold text-white flex items-center gap-1.5">
                    <span>Partage WhatsApp</span>
                    <span class="text-[10px] px-1.5 py-0.2 rounded bg-emerald-950 text-emerald-400 border border-emerald-800 font-semibold">Direct</span>
                  </h4>
                  <p class="text-[11px] text-slate-300 mt-0.5 leading-snug">
                    Synthèse structurée prête à l'envoi + transmission du fichier PDF sur smartphone ou WhatsApp Web.
                  </p>
                </div>
              </div>

              <div class="flex items-start gap-3 p-3 rounded-xl bg-slate-900/60 border border-slate-700/60">
                <div class="w-9 h-9 rounded-lg bg-sky-500/20 text-sky-400 flex items-center justify-center shrink-0">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                  </svg>
                </div>
                <div>
                  <h4 class="text-xs font-bold text-white flex items-center gap-1.5">
                    <span>Transmission E-mail</span>
                    <span class="text-[10px] px-1.5 py-0.2 rounded bg-sky-950 text-sky-400 border border-sky-800 font-semibold">Mailto</span>
                  </h4>
                  <p class="text-[11px] text-slate-300 mt-0.5 leading-snug">
                    Objet normalisé et corps de message récapitulatif complet pré-rempli dans votre messagerie.
                  </p>
                </div>
              </div>
            </div>

            <!-- Champ adresse email optionnelle -->
            <div class="pt-1">
              <label for="destinataireEmail" class="block text-xs font-bold text-slate-300 uppercase tracking-wider mb-1 flex items-center justify-between">
                <span>Adresse e-mail du destinataire <span class="text-slate-400 font-normal lowercase">(optionnel)</span></span>
                <span class="text-[10px] text-slate-400">ex: exploitation, régie, agence de l'eau</span>
              </label>
              <input
                type="email"
                id="destinataireEmail"
                placeholder="ex: exploitation@grand-bassin.fr"
                class="w-full px-3.5 py-2.5 text-xs sm:text-sm rounded-xl border border-slate-700 bg-slate-900/80 text-white placeholder:text-slate-500 focus:outline-none focus:ring-2 focus:ring-sky-500 transition"
              />
            </div>
          </div>

          <!-- Alertes globales d'erreurs -->
          <div id="validationBanner" class="hidden p-3.5 rounded-xl bg-rose-950/70 border border-rose-500/50 text-rose-200 text-xs">
            <div class="flex items-center gap-2 font-bold mb-1">
              <svg class="w-4 h-4 text-rose-400 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"/>
              </svg>
              <span>Veuillez compléter tous les champs obligatoires :</span>
            </div>
            <ul id="validationList" class="list-disc list-inside space-y-0.5 text-rose-300 pl-1"></ul>
          </div>

          <!-- Bouton principal de génération -->
          <div class="pt-2">
            <button
              type="submit"
              id="btnSubmit"
              class="w-full py-4 px-6 rounded-xl font-extrabold text-base sm:text-lg bg-gradient-to-r from-emerald-500 via-teal-600 to-sky-600 hover:from-emerald-400 hover:to-sky-500 active:scale-[0.99] text-white shadow-lg shadow-emerald-600/30 flex items-center justify-center gap-3 transition cursor-pointer"
            >
              <svg id="btnIconSend" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/>
              </svg>
              <!-- Spinner / Loader visuel -->
              <svg id="btnSpinner" class="w-6 h-6 animate-spin hidden text-white" fill="none" viewBox="0 0 24 24">
                <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
              </svg>
              <span id="btnText">Générer le Rapport PDF (Prêt pour WhatsApp &amp; Mail)</span>
            </button>
            <div class="flex flex-wrap items-center justify-center gap-3 text-xs text-slate-400 mt-2.5">
              <span class="text-[#25D366] font-medium">✓ Partage direct WhatsApp</span>
              <span>•</span>
              <span class="text-sky-300">✓ Envoi e-mail préparé</span>
              <span>•</span>
              <span class="text-slate-300">✓ Téléchargement direct</span>
            </div>
          </div>

          <!-- Panneau d'actions directes WhatsApp / Email / Téléchargement dans la Section 4 -->
          <div id="section4SharePanel" class="hidden p-3.5 rounded-xl bg-slate-900 border border-emerald-500/60 space-y-2.5">
            <div class="flex items-center justify-between text-xs">
              <span class="text-emerald-400 font-bold flex items-center gap-1.5">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                <span>Rapport PDF prêt pour l'envoi :</span>
              </span>
              <span id="section4FileName" class="font-mono text-slate-300 truncate max-w-[200px]"></span>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 pt-1">
              <button
                type="button"
                id="section4BtnWhatsApp"
                class="py-2.5 px-3 bg-[#25D366] hover:bg-[#20ba59] active:bg-[#1caa4f] text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition cursor-pointer shadow-md"
              >
                <svg class="w-4 h-4 fill-white" viewBox="0 0 24 24"><path d="M12.04 2c-5.46 0-9.91 4.45-9.91 9.91 0 1.75.46 3.45 1.32 4.95L2.05 22l5.25-1.38c1.45.79 3.08 1.21 4.74 1.21 5.46 0 9.91-4.45 9.91-9.91 0-2.65-1.03-5.14-2.9-7.01A9.816 9.816 0 0012.04 2zm.01 1.67c4.54 0 8.24 3.7 8.24 8.24 0 2.2-.86 4.27-2.42 5.82-1.55 1.56-3.62 2.42-5.82 2.42-1.48 0-2.93-.39-4.21-1.15l-.3-.18-3.12.82.83-3.04-.2-.31c-.83-1.32-1.27-2.86-1.27-4.38 0-4.54 3.7-8.24 8.24-8.24zm-3.62 4.75c-.2 0-.44.08-.66.32-.22.24-.86.84-.86 2.05s.88 2.38 1 2.55c.12.16 1.7 2.6 4.13 3.65.58.25 1.03.4 1.38.51.58.19 1.11.16 1.53.1.47-.07 1.44-.59 1.64-1.15.2-.57.2-1.05.14-1.15-.06-.1-.22-.16-.46-.28-.24-.12-1.44-.71-1.66-.79-.22-.08-.38-.12-.54.12-.16.24-.62.79-.76.95-.14.16-.28.18-.52.06-.24-.12-1.01-.37-1.92-1.19-.71-.63-1.19-1.41-1.33-1.65-.14-.24-.01-.37.11-.49.11-.11.24-.28.36-.42.12-.14.16-.24.24-.4.08-.16.04-.3-.02-.42-.06-.12-.54-1.3-.74-1.78-.19-.48-.39-.41-.54-.42h-.47z"/></svg>
                <span>Envoyer via WhatsApp</span>
              </button>
              <button
                type="button"
                id="section4BtnEmail"
                class="py-2.5 px-3 bg-sky-600 hover:bg-sky-500 active:bg-sky-700 text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition cursor-pointer shadow-md"
              >
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                <span>Envoyer par Email</span>
              </button>
              <button
                type="button"
                id="section4BtnDownload"
                class="py-2.5 px-3 bg-slate-800 hover:bg-slate-700 text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition cursor-pointer border border-slate-700 shadow-md"
              >
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"/></svg>
                <span>Télécharger le PDF</span>
              </button>
            </div>
          </div>
        </div>
      </section>

    </form>

  </main>

  <!-- Modal de confirmation / visualisation post-génération avec aperçu PDF -->
  <div id="successModal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden flex items-center justify-center p-2 sm:p-4">
    <div class="bg-white rounded-2xl max-w-4xl w-full max-h-[95vh] flex flex-col shadow-2xl overflow-hidden border border-slate-300">
      <div class="flex items-center justify-between p-4 bg-slate-900 text-white shrink-0">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-xl bg-emerald-500 text-white flex items-center justify-center shrink-0 shadow">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
          </div>
          <div>
            <h3 class="text-base sm:text-lg font-bold text-white flex items-center gap-2">
              Rapport PDF Officiel Généré
              <span class="text-xs px-2 py-0.5 rounded-full bg-emerald-900 text-emerald-300 font-normal">Photos incluses</span>
            </h3>
            <p id="modalFileName" class="text-xs text-slate-300 font-mono truncate max-w-[280px] sm:max-w-md"></p>
          </div>
        </div>
        <button id="modalBtnClose" type="button" class="p-1.5 rounded-lg text-slate-400 hover:text-white hover:bg-slate-800 transition cursor-pointer">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
      </div>

      <!-- Action Center Partage Direct WhatsApp & Mail -->
      <div class="p-4 bg-gradient-to-r from-slate-900 via-slate-800 to-slate-900 border-b border-slate-700 text-white shrink-0">
        <div class="flex flex-col md:flex-row items-stretch md:items-center justify-between gap-3">
          <div>
            <h4 class="text-sm font-bold text-white flex items-center gap-2">
              <span>Partager le Bilan Officiel</span>
              <span class="text-[10px] px-2 py-0.5 rounded-full bg-emerald-950 text-emerald-300 border border-emerald-700">Prêt</span>
            </h4>
            <p class="text-xs text-slate-300 mt-0.5">
              Fichier téléchargé sur votre appareil. Choisissez votre canal de transmission :
            </p>
          </div>

          <div class="flex flex-wrap items-center gap-2">
            <button id="modalBtnWhatsApp" type="button" class="flex-1 sm:flex-initial py-2.5 px-4 bg-[#25D366] hover:bg-[#20ba59] text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition cursor-pointer shadow-md">
              <svg class="w-4 h-4 fill-white" viewBox="0 0 24 24"><path d="M12.04 2c-5.46 0-9.91 4.45-9.91 9.91 0 1.75.46 3.45 1.32 4.95L2.05 22l5.25-1.38c1.45.79 3.08 1.21 4.74 1.21 5.46 0 9.91-4.45 9.91-9.91 0-2.65-1.03-5.14-2.9-7.01A9.816 9.816 0 0012.04 2zm.01 1.67c4.54 0 8.24 3.7 8.24 8.24 0 2.2-.86 4.27-2.42 5.82-1.55 1.56-3.62 2.42-5.82 2.42-1.48 0-2.93-.39-4.21-1.15l-.3-.18-3.12.82.83-3.04-.2-.31c-.83-1.32-1.27-2.86-1.27-4.38 0-4.54 3.7-8.24 8.24-8.24zm-3.62 4.75c-.2 0-.44.08-.66.32-.22.24-.86.84-.86 2.05s.88 2.38 1 2.55c.12.16 1.7 2.6 4.13 3.65.58.25 1.03.4 1.38.51.58.19 1.11.16 1.53.1.47-.07 1.44-.59 1.64-1.15.2-.57.2-1.05.14-1.15-.06-.1-.22-.16-.46-.28-.24-.12-1.44-.71-1.66-.79-.22-.08-.38-.12-.54.12-.16.24-.62.79-.76.95-.14.16-.28.18-.52.06-.24-.12-1.01-.37-1.92-1.19-.71-.63-1.19-1.41-1.33-1.65-.14-.24-.01-.37.11-.49.11-.11.24-.28.36-.42.12-.14.16-.24.24-.4.08-.16.04-.3-.02-.42-.06-.12-.54-1.3-.74-1.78-.19-.48-.39-.41-.54-.42h-.47z"/></svg>
              <span>Envoyer via WhatsApp</span>
            </button>
            <button id="modalBtnEmail" type="button" class="flex-1 sm:flex-initial py-2.5 px-4 bg-sky-600 hover:bg-sky-500 text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition cursor-pointer shadow-md">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
              <span>Envoyer par Email</span>
            </button>
            <button id="modalBtnCopy" type="button" class="py-2.5 px-3 bg-slate-800 hover:bg-slate-700 text-slate-200 font-medium rounded-xl flex items-center justify-center gap-1.5 text-xs transition border border-slate-700 cursor-pointer">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"/></svg>
              <span id="modalCopyText">Copier la synthèse</span>
            </button>
          </div>
        </div>
      </div>

      <!-- Ruban confirmation photos -->
      <div class="bg-slate-50 border-b border-slate-200 px-4 py-2.5 flex flex-wrap items-center justify-between gap-3 text-xs text-slate-700 shrink-0">
        <div class="flex items-center gap-4">
          <span class="font-semibold text-slate-900">Photos intégrées au document PDF :</span>
          <span class="text-sky-700 font-medium">✓ Photo Entrée</span>
          <span class="text-emerald-700 font-medium">✓ Photo Sortie</span>
        </div>
        <div class="text-slate-500">Téléchargement : <strong class="text-emerald-700">Enregistré dans vos téléchargements</strong></div>
      </div>

      <!-- Iframe aperçu PDF -->
      <div class="flex-1 min-h-[350px] sm:min-h-[460px] bg-slate-200 relative p-2">
        <iframe id="modalPdfFrame" src="" class="w-full h-full rounded-xl border border-slate-300 bg-white shadow-inner"></iframe>
      </div>

      <!-- Actions bas de modale -->
      <div class="p-4 bg-white border-t border-slate-200 flex flex-col sm:flex-row items-center justify-between gap-3 shrink-0">
        <div class="flex flex-wrap items-center gap-2 w-full sm:w-auto">
          <button id="modalBtnDownload" type="button" class="flex-1 sm:flex-initial py-2.5 px-4 bg-slate-800 hover:bg-slate-700 text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition shadow-sm cursor-pointer">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"/></svg>
            Télécharger le PDF
          </button>
          <button type="button" id="modalBtnFooterWhatsApp" class="flex-1 sm:flex-initial py-2.5 px-4 bg-[#25D366] hover:bg-[#20ba59] text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition shadow-sm cursor-pointer">
            <svg class="w-4 h-4 fill-white" viewBox="0 0 24 24"><path d="M12.04 2c-5.46 0-9.91 4.45-9.91 9.91 0 1.75.46 3.45 1.32 4.95L2.05 22l5.25-1.38c1.45.79 3.08 1.21 4.74 1.21 5.46 0 9.91-4.45 9.91-9.91 0-2.65-1.03-5.14-2.9-7.01A9.816 9.816 0 0012.04 2zm.01 1.67c4.54 0 8.24 3.7 8.24 8.24 0 2.2-.86 4.27-2.42 5.82-1.55 1.56-3.62 2.42-5.82 2.42-1.48 0-2.93-.39-4.21-1.15l-.3-.18-3.12.82.83-3.04-.2-.31c-.83-1.32-1.27-2.86-1.27-4.38 0-4.54 3.7-8.24 8.24-8.24zm-3.62 4.75c-.2 0-.44.08-.66.32-.22.24-.86.84-.86 2.05s.88 2.38 1 2.55c.12.16 1.7 2.6 4.13 3.65.58.25 1.03.4 1.38.51.58.19 1.11.16 1.53.1.47-.07 1.44-.59 1.64-1.15.2-.57.2-1.05.14-1.15-.06-.1-.22-.16-.46-.28-.24-.12-1.44-.71-1.66-.79-.22-.08-.38-.12-.54.12-.16.24-.62.79-.76.95-.14.16-.28.18-.52.06-.24-.12-1.01-.37-1.92-1.19-.71-.63-1.19-1.41-1.33-1.65-.14-.24-.01-.37.11-.49.11-.11.24-.28.36-.42.12-.14.16-.24.24-.4.08-.16.04-.3-.02-.42-.06-.12-.54-1.3-.74-1.78-.19-.48-.39-.41-.54-.42h-.47z"/></svg>
            <span>WhatsApp</span>
          </button>
          <button type="button" id="modalBtnFooterEmail" class="flex-1 sm:flex-initial py-2.5 px-4 bg-sky-600 hover:bg-sky-500 text-white font-bold rounded-xl flex items-center justify-center gap-2 text-xs transition shadow-sm cursor-pointer">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
            <span>Email</span>
          </button>
        </div>
        <button id="modalBtnBottomClose" type="button" class="text-xs text-slate-500 hover:text-slate-800 font-medium py-1 px-3 cursor-pointer">
          Fermer l'aperçu
        </button>
      </div>
    </div>
  </div>

  <!-- Pied de page avec mention obligatoire "Créé par Laurent Juillien" -->
  <footer class="bg-white border-t border-slate-200 mt-auto py-5 px-4">
    <div class="max-w-4xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-2 text-xs text-slate-500">
      <div class="flex items-center gap-2">
        <span class="inline-block w-2 h-2 rounded-full bg-emerald-500"></span>
        <span>Autosurveillance STEP • Application Métier Terrain</span>
      </div>
      <div class="font-bold text-slate-700 text-sm">
        Créé par Laurent Juillien
      </div>
    </div>
  </footer>

  <!-- SCRIPT LOGIQUE APPLICATIVE -->
  <script>
    (function() {
      // Données en mémoire
      const state = {
        entreePhoto: null,
        sortiePhoto: null,
        lastBlob: null,
        lastFileName: '',
        lastPdfRes: null
      };

      // Éléments DOM
      const form = document.getElementById('stepForm');
      const nomStep = document.getElementById('nomStep');
      const dateAutosurveillance = document.getElementById('dateAutosurveillance');
      const technicienNom = document.getElementById('technicienNom');
      const meteo = document.getElementById('meteo');
      const observations = document.getElementById('observations');
      const destinataireEmail = document.getElementById('destinataireEmail');

      const entreeDate = document.getElementById('entreeDate');
      const entreeHeure = document.getElementById('entreeHeure');
      const entreeTemperature = document.getElementById('entreeTemperature');
      const entreeDebit = document.getElementById('entreeDebit');
      const entreePhotoInput = document.getElementById('entreePhotoInput');
      const entreePhotoBox = document.getElementById('entreePhotoBox');
      const entreePlaceholder = document.getElementById('entreePlaceholder');
      const entreePreviewContainer = document.getElementById('entreePreviewContainer');
      const entreePreviewImg = document.getElementById('entreePreviewImg');
      const btnDeleteEntreePhoto = document.getElementById('btnDeleteEntreePhoto');
      const btnChangeEntreePhoto = document.getElementById('btnChangeEntreePhoto');

      const sortieDate = document.getElementById('sortieDate');
      const sortieHeure = document.getElementById('sortieHeure');
      const sortieTemperature = document.getElementById('sortieTemperature');
      const sortieDebit = document.getElementById('sortieDebit');
      const sortiePhotoInput = document.getElementById('sortiePhotoInput');
      const sortiePhotoBox = document.getElementById('sortiePhotoBox');
      const sortiePlaceholder = document.getElementById('sortiePlaceholder');
      const sortiePreviewContainer = document.getElementById('sortiePreviewContainer');
      const sortiePreviewImg = document.getElementById('sortiePreviewImg');
      const btnDeleteSortiePhoto = document.getElementById('btnDeleteSortiePhoto');
      const btnChangeSortiePhoto = document.getElementById('btnChangeSortiePhoto');

      const btnSubmit = document.getElementById('btnSubmit');
      const btnText = document.getElementById('btnText');
      const btnIconSend = document.getElementById('btnIconSend');
      const btnSpinner = document.getElementById('btnSpinner');
      const validationBanner = document.getElementById('validationBanner');
      const validationList = document.getElementById('validationList');

      const section4SharePanel = document.getElementById('section4SharePanel');
      const section4FileName = document.getElementById('section4FileName');
      const section4BtnWhatsApp = document.getElementById('section4BtnWhatsApp');
      const section4BtnEmail = document.getElementById('section4BtnEmail');
      const section4BtnDownload = document.getElementById('section4BtnDownload');

      const successModal = document.getElementById('successModal');
      const modalFileName = document.getElementById('modalFileName');
      const modalBtnClose = document.getElementById('modalBtnClose');
      const modalBtnBottomClose = document.getElementById('modalBtnBottomClose');
      const modalBtnDownload = document.getElementById('modalBtnDownload');
      const modalBtnWhatsApp = document.getElementById('modalBtnWhatsApp');
      const modalBtnEmail = document.getElementById('modalBtnEmail');
      const modalBtnCopy = document.getElementById('modalBtnCopy');
      const modalCopyText = document.getElementById('modalCopyText');
      const modalBtnFooterWhatsApp = document.getElementById('modalBtnFooterWhatsApp');
      const modalBtnFooterEmail = document.getElementById('modalBtnFooterEmail');

      const btnExemple = document.getElementById('btnExemple');
      const btnReset = document.getElementById('btnReset');

      // Initialiser la date du jour par défaut
      const today = new Date().toISOString().split('T')[0];
      dateAutosurveillance.value = today;
      entreeDate.value = today;
      sortieDate.value = today;

      // Heure courante par défaut
      const now = new Date();
      const currentHours = String(now.getHours()).padStart(2, '0');
      const currentMins = String(Math.floor(now.getMinutes() / 5) * 5).padStart(2, '0');
      entreeHeure.value = `${currentHours}:${currentMins}`;
      sortieHeure.value = `${currentHours}:${currentMins}`;

      // Compression d'image dans Canvas pour la fluidité mobile
      function processImage(file) {
        return new Promise(function(resolve, reject) {
          const reader = new FileReader();
          reader.onerror = reject;
          reader.onload = function(e) {
            const img = new Image();
            img.onerror = reject;
            img.onload = function() {
              const maxWidth = 1200;
              const maxHeight = 900;
              let width = img.width;
              let height = img.height;

              if (width > maxWidth || height > maxHeight) {
                const ratio = Math.min(maxWidth / width, maxHeight / height);
                width = Math.round(width * ratio);
                height = Math.round(height * ratio);
              }

              const canvas = document.createElement('canvas');
              canvas.width = width;
              canvas.height = height;
              const ctx = canvas.getContext('2d');
              ctx.imageSmoothingEnabled = true;
              ctx.imageSmoothingQuality = 'high';
              ctx.drawImage(img, 0, 0, width, height);

              resolve(canvas.toDataURL('image/jpeg', 0.82));
            };
            img.src = e.target.result;
          };
          reader.readAsDataURL(file);
        });
      }

      // Gestion Photo Entrée
      entreePhotoBox.addEventListener('click', function(e) {
        if (e.target === btnDeleteEntreePhoto || btnDeleteEntreePhoto.contains(e.target)) return;
        entreePhotoInput.click();
      });

      entreePhotoInput.addEventListener('change', async function() {
        if (!this.files || !this.files[0]) return;
        try {
          const compressed = await processImage(this.files[0]);
          state.entreePhoto = compressed;
          entreePreviewImg.src = compressed;
          entreePlaceholder.classList.add('hidden');
          entreePreviewContainer.classList.remove('hidden');
          clearError('entreePhoto');
        } catch (err) {
          alert("Erreur lors de la lecture de la photo : " + err.message);
        }
      });

      btnDeleteEntreePhoto.addEventListener('click', function(e) {
        e.stopPropagation();
        state.entreePhoto = null;
        entreePhotoInput.value = '';
        entreePreviewImg.src = '';
        entreePreviewContainer.classList.add('hidden');
        entreePlaceholder.classList.remove('hidden');
      });

      btnChangeEntreePhoto.addEventListener('click', function(e) {
        e.stopPropagation();
        entreePhotoInput.click();
      });

      // Gestion Photo Sortie
      sortiePhotoBox.addEventListener('click', function(e) {
        if (e.target === btnDeleteSortiePhoto || btnDeleteSortiePhoto.contains(e.target)) return;
        sortiePhotoInput.click();
      });

      sortiePhotoInput.addEventListener('change', async function() {
        if (!this.files || !this.files[0]) return;
        try {
          const compressed = await processImage(this.files[0]);
          state.sortiePhoto = compressed;
          sortiePreviewImg.src = compressed;
          sortiePlaceholder.classList.add('hidden');
          sortiePreviewContainer.classList.remove('hidden');
          clearError('sortiePhoto');
        } catch (err) {
          alert("Erreur lors de la lecture de la photo : " + err.message);
        }
      });

      btnDeleteSortiePhoto.addEventListener('click', function(e) {
        e.stopPropagation();
        state.sortiePhoto = null;
        sortiePhotoInput.value = '';
        sortiePreviewImg.src = '';
        sortiePreviewContainer.classList.add('hidden');
        sortiePlaceholder.classList.remove('hidden');
      });

      btnChangeSortiePhoto.addEventListener('click', function(e) {
        e.stopPropagation();
        sortiePhotoInput.click();
      });

      // Gestion des erreurs de formulaire
      function showError(fieldId, message) {
        const errEl = document.getElementById('err-' + fieldId);
        if (errEl) {
          errEl.textContent = message;
          errEl.classList.remove('hidden');
        }
        const inputEl = document.getElementById(fieldId);
        if (inputEl) {
          inputEl.classList.add('border-rose-500', 'bg-rose-50/40');
        }
      }

      function clearError(fieldId) {
        const errEl = document.getElementById('err-' + fieldId);
        if (errEl) {
          errEl.textContent = '';
          errEl.classList.add('hidden');
        }
        const inputEl = document.getElementById(fieldId);
        if (inputEl) {
          inputEl.classList.remove('border-rose-500', 'bg-rose-50/40');
        }
      }

      // Nettoyer l'erreur lors de la saisie
      ['nomStep', 'dateAutosurveillance', 'entreeDate', 'entreeHeure', 'entreeTemperature', 'entreeDebit', 'sortieDate', 'sortieHeure', 'sortieTemperature', 'sortieDebit'].forEach(function(id) {
        const el = document.getElementById(id);
        if (el) {
          el.addEventListener('input', function() { clearError(id); });
        }
      });

      // Validation stricte du formulaire terrain
      function validateForm() {
        const errors = [];
        validationBanner.classList.add('hidden');
        validationList.innerHTML = '';

        if (!nomStep.value.trim()) {
          showError('nomStep', 'Le nom de la STEP est obligatoire');
          errors.push("Nom de la station d'épuration (STEP)");
        } else {
          clearError('nomStep');
        }

        if (!dateAutosurveillance.value) {
          showError('dateAutosurveillance', 'La date de bilan est obligatoire');
          errors.push("Date de l'autosurveillance");
        } else {
          clearError('dateAutosurveillance');
        }

        // Entrée
        if (!entreeDate.value) {
          showError('entreeDate', 'Date obligatoire');
          errors.push("Entrée : Date de prélèvement");
        }
        if (!entreeHeure.value) {
          showError('entreeHeure', 'Heure obligatoire');
          errors.push("Entrée : Heure de relève");
        }
        if (entreeTemperature.value === '') {
          showError('entreeTemperature', 'Température obligatoire');
          errors.push("Entrée : Température préleveur");
        }
        if (entreeDebit.value === '' || parseFloat(entreeDebit.value) < 0) {
          showError('entreeDebit', 'Débit valide obligatoire (>= 0)');
          errors.push("Entrée : Débit écoulé sur 24h");
        }
        if (!state.entreePhoto) {
          showError('entreePhoto', 'Photo du préleveur Entrée obligatoire');
          errors.push("Entrée : Photo du préleveur / flacons");
        }

        // Sortie
        if (!sortieDate.value) {
          showError('sortieDate', 'Date obligatoire');
          errors.push("Sortie : Date de prélèvement");
        }
        if (!sortieHeure.value) {
          showError('sortieHeure', 'Heure obligatoire');
          errors.push("Sortie : Heure de relève");
        }
        if (sortieTemperature.value === '') {
          showError('sortieTemperature', 'Température obligatoire');
          errors.push("Sortie : Température préleveur");
        }
        if (sortieDebit.value === '' || parseFloat(sortieDebit.value) < 0) {
          showError('sortieDebit', 'Débit valide obligatoire (>= 0)');
          errors.push("Sortie : Débit écoulé sur 24h");
        }
        if (!state.sortiePhoto) {
          showError('sortiePhoto', 'Photo du préleveur Sortie obligatoire');
          errors.push("Sortie : Photo du préleveur / rejet");
        }

        if (errors.length > 0) {
          errors.forEach(function(msg) {
            const li = document.createElement('li');
            li.textContent = msg;
            validationList.appendChild(li);
          });
          validationBanner.classList.remove('hidden');
          validationBanner.scrollIntoView({ behavior: 'smooth', block: 'center' });
          return false;
        }

        return true;
      }

      // Helper pour charger et préparer l'image dans un canvas avec ratio exact
      function prepareCanvasImage(dataUrl) {
        if (!dataUrl) return Promise.resolve(null);
        return new Promise(function(resolve) {
          const img = new Image();
          img.crossOrigin = 'anonymous';
          img.onload = function() {
            const w = img.naturalWidth || img.width || 800;
            const h = img.naturalHeight || img.height || 600;
            const canvas = document.createElement('canvas');
            canvas.width = w;
            canvas.height = h;
            const ctx = canvas.getContext('2d');
            ctx.fillStyle = '#ffffff';
            ctx.fillRect(0, 0, w, h);
            ctx.drawImage(img, 0, 0, w, h);
            resolve({ canvas: canvas, ratio: w / h });
          };
          img.onerror = function() {
            resolve(null);
          };
          img.src = dataUrl;
        });
      }

      // Génération du PDF avec jsPDF
      async function buildPdf() {
        const { jsPDF } = window.jspdf;
        const doc = new jsPDF({
          orientation: 'portrait',
          unit: 'mm',
          format: 'a4',
          compress: true
        });

        const [entreeImg, sortieImg] = await Promise.all([
          prepareCanvasImage(state.entreePhoto),
          prepareCanvasImage(state.sortiePhoto)
        ]);

        const pageWidth = 210;
        const pageHeight = 297;
        const margin = 12;
        const contentWidth = pageWidth - margin * 2; // 186mm

        const primary = [15, 76, 129];
        const secondary = [2, 132, 199];
        const entreeColor = [3, 105, 161];
        const sortieColor = [5, 150, 105];
        const textSlate = [30, 41, 59];
        const muted = [100, 116, 139];

        // En-tête officiel
        doc.setFillColor(primary[0], primary[1], primary[2]);
        doc.rect(margin, 10, contentWidth, 20, 'F');
        doc.setFillColor(secondary[0], secondary[1], secondary[2]);
        doc.rect(margin, 30, contentWidth, 2, 'F');

        doc.setTextColor(255, 255, 255);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(13);
        doc.text("BILAN D'AUTOSURVEILLANCE 24H — STATION D'ÉPURATION", margin + 5, 18);

        doc.setFont('helvetica', 'normal');
        doc.setFontSize(8.5);
        doc.text("CONTRÔLE RÉGLEMENTAIRE TERRAIN • PRÉLÈVEMENTS & MESURES OFFICIELLES", margin + 5, 25);

        const nowFormatted = new Date().toLocaleDateString('fr-FR');
        doc.setFontSize(7.5);
        doc.text(`Réf : AS-${(dateAutosurveillance.value || '').replace(/-/g, '')}`, pageWidth - margin - 5, 18, { align: 'right' });
        doc.text(`Édité le : ${nowFormatted} ${new Date().toLocaleTimeString('fr-FR', { hour: '2-digit', minute: '2-digit' })}`, pageWidth - margin - 5, 25, { align: 'right' });

        let curY = 36;

        // Fiche Station
        doc.setFillColor(248, 250, 252);
        doc.setDrawColor(226, 232, 240);
        doc.roundedRect(margin, curY, contentWidth, 17, 2, 2, 'FD');

        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8.5);
        doc.setTextColor(primary[0], primary[1], primary[2]);
        doc.text("STATION D'ÉPURATION :", margin + 4, curY + 6);

        doc.setFont('helvetica', 'bold');
        doc.setFontSize(11);
        doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
        doc.text((nomStep.value || 'NON SPÉCIFIÉ').toUpperCase(), margin + 46, curY + 6);

        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8);
        doc.setTextColor(muted[0], muted[1], muted[2]);
        doc.text("Date du bilan :", margin + 4, curY + 12.5);
        doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
        doc.text(dateAutosurveillance.value, margin + 26, curY + 12.5);

        if (technicienNom.value) {
          doc.setTextColor(muted[0], muted[1], muted[2]);
          doc.setFont('helvetica', 'normal');
          doc.text("Technicien :", margin + 85, curY + 12.5);
          doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.text(technicienNom.value, margin + 103, curY + 12.5);
        }

        if (meteo.value) {
          doc.setTextColor(muted[0], muted[1], muted[2]);
          doc.setFont('helvetica', 'normal');
          doc.text("Météo :", margin + 145, curY + 12.5);
          doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.text(meteo.value, margin + 158, curY + 12.5);
        }

        curY += 21;

        // Blocs Entrée & Sortie
        const colWidth = (contentWidth - 6) / 2;
        const colEntreeX = margin;
        const colSortieX = margin + colWidth + 6;
        const blockHeight = 44;

        // Entrée
        doc.setFillColor(240, 249, 255);
        doc.setDrawColor(186, 230, 253);
        doc.roundedRect(colEntreeX, curY, colWidth, blockHeight, 2, 2, 'FD');

        doc.setFillColor(entreeColor[0], entreeColor[1], entreeColor[2]);
        doc.roundedRect(colEntreeX, curY, colWidth, 7, 2, 2, 'F');
        doc.rect(colEntreeX, curY + 3, colWidth, 4, 'F');
        doc.setTextColor(255, 255, 255);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(9.5);
        doc.text("BILAN ENTRÉE (Eaux Brutes)", colEntreeX + 4, curY + 5);

        const rowsEntree = [
          { l: "Date prélèvement", v: entreeDate.value },
          { l: "Heure relève", v: entreeHeure.value },
          { l: "Température préleveur", v: `${entreeTemperature.value} °C`, s: (parseFloat(entreeTemperature.value) >= 2 && parseFloat(entreeTemperature.value) <= 5) ? "Conforme (2-5°C)" : "Hors cible (2-5°C)" },
          { l: "Débit écoulé 24h", v: `${Number(entreeDebit.value).toLocaleString('fr-FR')} m³`, h: true }
        ];

        let rY = curY + 13;
        rowsEntree.forEach(r => {
          doc.setTextColor(muted[0], muted[1], muted[2]);
          doc.setFont('helvetica', 'normal');
          doc.setFontSize(8);
          doc.text(r.l, colEntreeX + 4, rY);
          doc.setTextColor(r.h ? entreeColor[0] : textSlate[0], r.h ? entreeColor[1] : textSlate[1], r.h ? entreeColor[2] : textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.setFontSize(r.h ? 10 : 8.5);
          doc.text(r.v, colEntreeX + colWidth - 4, rY, { align: 'right' });
          if (r.s) {
            doc.setFontSize(6.5);
            doc.setTextColor(muted[0], muted[1], muted[2]);
            doc.text(r.s, colEntreeX + colWidth - 4, rY + 3.2, { align: 'right' });
          }
          rY += 7.8;
        });

        // Sortie
        doc.setFillColor(236, 253, 245);
        doc.setDrawColor(167, 243, 208);
        doc.roundedRect(colSortieX, curY, colWidth, blockHeight, 2, 2, 'FD');

        doc.setFillColor(sortieColor[0], sortieColor[1], sortieColor[2]);
        doc.roundedRect(colSortieX, curY, colWidth, 7, 2, 2, 'F');
        doc.rect(colSortieX, curY + 3, colWidth, 4, 'F');
        doc.setTextColor(255, 255, 255);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(9.5);
        doc.text("BILAN SORTIE (Rejet Traité)", colSortieX + 4, curY + 5);

        const rowsSortie = [
          { l: "Date prélèvement", v: sortieDate.value },
          { l: "Heure relève", v: sortieHeure.value },
          { l: "Température préleveur", v: `${sortieTemperature.value} °C`, s: (parseFloat(sortieTemperature.value) >= 2 && parseFloat(sortieTemperature.value) <= 5) ? "Conforme (2-5°C)" : "Hors cible (2-5°C)" },
          { l: "Débit écoulé 24h", v: `${Number(sortieDebit.value).toLocaleString('fr-FR')} m³`, h: true }
        ];

        rY = curY + 13;
        rowsSortie.forEach(r => {
          doc.setTextColor(muted[0], muted[1], muted[2]);
          doc.setFont('helvetica', 'normal');
          doc.setFontSize(8);
          doc.text(r.l, colSortieX + 4, rY);
          doc.setTextColor(r.h ? sortieColor[0] : textSlate[0], r.h ? sortieColor[1] : textSlate[1], r.h ? sortieColor[2] : textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.setFontSize(r.h ? 10 : 8.5);
          doc.text(r.v, colSortieX + colWidth - 4, rY, { align: 'right' });
          if (r.s) {
            doc.setFontSize(6.5);
            doc.setTextColor(muted[0], muted[1], muted[2]);
            doc.text(r.s, colSortieX + colWidth - 4, rY + 3.2, { align: 'right' });
          }
          rY += 7.8;
        });

        curY += blockHeight + 5;

        // Bilan Volumétrique
        const qIn = parseFloat(entreeDebit.value);
        const qOut = parseFloat(sortieDebit.value);
        let volumetrie = "Calcul volumétrique : Enregistrement conforme 24h.";
        if (qIn > 0 && !isNaN(qOut)) {
          const diff = qOut - qIn;
          const ratio = ((qOut / qIn) * 100).toFixed(1);
          volumetrie = `Calcul volumétrique : Débit Sortie / Débit Entrée = ${ratio}% (Écart : ${diff > 0 ? '+' : ''}${diff.toFixed(1)} m³)`;
        }

        doc.setFillColor(241, 245, 249);
        doc.setDrawColor(203, 213, 225);
        doc.roundedRect(margin, curY, contentWidth, 8, 1.5, 1.5, 'FD');
        doc.setTextColor(primary[0], primary[1], primary[2]);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8);
        doc.text(volumetrie, margin + 4, curY + 5.2);

        curY += 12;

        // Section Photographies avec horodatage
        const photoHeight = 100;
        const photoWidth = (contentWidth - 6) / 2;

        // Cadre Entrée
        doc.setFillColor(255, 255, 255);
        doc.setDrawColor(203, 213, 225);
        doc.roundedRect(colEntreeX, curY, photoWidth, photoHeight, 2, 2, 'FD');

        doc.setFillColor(entreeColor[0], entreeColor[1], entreeColor[2]);
        doc.roundedRect(colEntreeX, curY, photoWidth, 6, 2, 2, 'F');
        doc.rect(colEntreeX, curY + 2, photoWidth, 4, 'F');
        doc.setTextColor(255, 255, 255);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8);
        doc.text("PHOTO PRÉLEVEUR ENTRÉE", colEntreeX + 3, curY + 4.3);

        const imgAreaEntreeX = colEntreeX + 2;
        const imgAreaEntreeY = curY + 8;
        const maxImgW = photoWidth - 4;
        const maxImgH = photoHeight - 16;

        if (entreeImg) {
          let renderW = maxImgW;
          let renderH = renderW / entreeImg.ratio;
          if (renderH > maxImgH) {
            renderH = maxImgH;
            renderW = renderH * entreeImg.ratio;
          }
          const posX = imgAreaEntreeX + (maxImgW - renderW) / 2;
          const posY = imgAreaEntreeY + (maxImgH - renderH) / 2;

          doc.setDrawColor(226, 232, 240);
          doc.setFillColor(241, 245, 249);
          doc.rect(imgAreaEntreeX, imgAreaEntreeY, maxImgW, maxImgH, 'F');

          doc.addImage(entreeImg.canvas, 'JPEG', posX, posY, renderW, renderH, undefined, 'FAST');
          doc.setDrawColor(203, 213, 225);
          doc.rect(posX, posY, renderW, renderH, 'D');

          doc.setFillColor(248, 250, 252);
          doc.rect(colEntreeX + 1, curY + photoHeight - 6.5, photoWidth - 2, 5.5, 'F');
          doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.setFontSize(6.5);
          doc.text(`Prise le ${entreeDate.value} à ${entreeHeure.value} • T: ${entreeTemperature.value}°C • Q: ${entreeDebit.value} m³`, colEntreeX + 3, curY + photoHeight - 2.5);
        } else {
          doc.setTextColor(160, 174, 192);
          doc.setFont('helvetica', 'italic');
          doc.setFontSize(8);
          doc.text("Aucune photo capturée", colEntreeX + photoWidth / 2, curY + 45, { align: 'center' });
        }

        // Cadre Sortie
        doc.setFillColor(255, 255, 255);
        doc.setDrawColor(203, 213, 225);
        doc.roundedRect(colSortieX, curY, photoWidth, photoHeight, 2, 2, 'FD');

        doc.setFillColor(sortieColor[0], sortieColor[1], sortieColor[2]);
        doc.roundedRect(colSortieX, curY, photoWidth, 6, 2, 2, 'F');
        doc.rect(colSortieX, curY + 2, photoWidth, 4, 'F');
        doc.setTextColor(255, 255, 255);
        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8);
        doc.text("PHOTO PRÉLEVEUR SORTIE", colSortieX + 3, curY + 4.3);

        const imgAreaSortieX = colSortieX + 2;
        const imgAreaSortieY = curY + 8;

        if (sortieImg) {
          let renderW = maxImgW;
          let renderH = renderW / sortieImg.ratio;
          if (renderH > maxImgH) {
            renderH = maxImgH;
            renderW = renderH * sortieImg.ratio;
          }
          const posX = imgAreaSortieX + (maxImgW - renderW) / 2;
          const posY = imgAreaSortieY + (maxImgH - renderH) / 2;

          doc.setDrawColor(226, 232, 240);
          doc.setFillColor(241, 245, 249);
          doc.rect(imgAreaSortieX, imgAreaSortieY, maxImgW, maxImgH, 'F');

          doc.addImage(sortieImg.canvas, 'JPEG', posX, posY, renderW, renderH, undefined, 'FAST');
          doc.setDrawColor(203, 213, 225);
          doc.rect(posX, posY, renderW, renderH, 'D');

          doc.setFillColor(248, 250, 252);
          doc.rect(colSortieX + 1, curY + photoHeight - 6.5, photoWidth - 2, 5.5, 'F');
          doc.setTextColor(textSlate[0], textSlate[1], textSlate[2]);
          doc.setFont('helvetica', 'bold');
          doc.setFontSize(6.5);
          doc.text(`Prise le ${sortieDate.value} à ${sortieHeure.value} • T: ${sortieTemperature.value}°C • Q: ${sortieDebit.value} m³`, colSortieX + 3, curY + photoHeight - 2.5);
        } else {
          doc.setTextColor(160, 174, 192);
          doc.setFont('helvetica', 'italic');
          doc.setFontSize(8);
          doc.text("Aucune photo capturée", colSortieX + photoWidth / 2, curY + 45, { align: 'center' });
        }

        curY += photoHeight + 4;

        // Observations si existantes
        if (observations.value.trim()) {
          doc.setFillColor(254, 252, 232);
          doc.setDrawColor(254, 240, 138);
          doc.roundedRect(margin, curY, contentWidth, 13, 1.5, 1.5, 'FD');
          doc.setTextColor(146, 64, 14);
          doc.setFont('helvetica', 'bold');
          doc.setFontSize(7.5);
          doc.text("Remarques / Observations d'exploitation :", margin + 3, curY + 4.5);
          doc.setFont('helvetica', 'normal');
          doc.setFontSize(7);
          doc.setTextColor(50, 50, 50);
          const splitObs = doc.splitTextToSize(observations.value.trim(), contentWidth - 8);
          doc.text(splitObs.slice(0, 2), margin + 3, curY + 9);
        }

        // Pied de page officiel avec mention obligatoire : "Créé par Laurent Juillien"
        const footerY = pageHeight - 12;
        doc.setDrawColor(226, 232, 240);
        doc.line(margin, footerY - 2.5, pageWidth - margin, footerY - 2.5);

        doc.setFont('helvetica', 'normal');
        doc.setFontSize(7);
        doc.setTextColor(muted[0], muted[1], muted[2]);
        doc.text("Transmission réglementaire : Bilan d'autosurveillance STEP 24h", margin, footerY);
        doc.text("Fiche certifiée conforme — Prélèvements 24h avec mesures et photos horodatées", margin, footerY + 3.5);

        doc.setFont('helvetica', 'bold');
        doc.setFontSize(8.5);
        doc.setTextColor(primary[0], primary[1], primary[2]);
        doc.text("Créé par Laurent Juillien", pageWidth - margin, footerY + 2, { align: 'right' });

        const blob = doc.output('blob');
        const dataUri = doc.output('datauristring');
        const cleanName = nomStep.value.trim().replace(/[^a-zA-Z0-9_-]/g, '_') || 'STEP';
        const cleanDate = dateAutosurveillance.value.replace(/-/g, '');
        const fileName = `Bilan_Autosurveillance_${cleanName}_${cleanDate}.pdf`;

        return { blob, dataUri, fileName };
      }

      // Téléchargement direct du fichier PDF
      function downloadFile(blob, fileName) {
        const link = document.createElement('a');
        link.href = URL.createObjectURL(blob);
        link.download = fileName;
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
        setTimeout(() => URL.revokeObjectURL(link.href), 10000);
      }

      // Génération de la synthèse texte formatée pour WhatsApp et Email
      function generateReportSummary() {
        const hasDebits = entreeDebit.value && sortieDebit.value && !isNaN(Number(entreeDebit.value)) && !isNaN(Number(sortieDebit.value)) && Number(entreeDebit.value) > 0;
        const ratio = hasDebits ? ((Number(sortieDebit.value) / Number(entreeDebit.value)) * 100).toFixed(1) : null;
        const delta = hasDebits ? (Number(sortieDebit.value) - Number(entreeDebit.value)).toFixed(1) : null;

        const lines = [
          '📋 *BILAN D\'AUTOSURVEILLANCE STEP 24H*',
          '--------------------------------------',
          '🏢 *Station* : ' + (nomStep.value || 'Non précisée'),
          '📅 *Date du bilan* : ' + (dateAutosurveillance.value || 'Non précisée')
        ];
        if (technicienNom.value) lines.push('👷 *Technicien* : ' + technicienNom.value);
        if (meteo.value) lines.push('⛅ *Météo* : ' + meteo.value);

        lines.push('');
        lines.push('🔹 *ENTRÉE (Eaux Brutes)*');
        lines.push('  • Relève : ' + (entreeHeure.value || '-') + ' (' + (entreeDate.value || '-') + ')');
        lines.push('  • Température : ' + (entreeTemperature.value ? entreeTemperature.value + ' °C' : '-'));
        lines.push('  • Débit 24h : ' + (entreeDebit.value ? Number(entreeDebit.value).toLocaleString('fr-FR') + ' m³' : '-'));
        lines.push('  • Photo préleveur : ' + (state.entreePhoto ? '✓ Capturée' : 'Non jointe'));

        lines.push('');
        lines.push('🔹 *SORTIE (Eaux Traitées / Rejet)*');
        lines.push('  • Relève : ' + (sortieHeure.value || '-') + ' (' + (sortieDate.value || '-') + ')');
        lines.push('  • Température : ' + (sortieTemperature.value ? sortieTemperature.value + ' °C' : '-'));
        lines.push('  • Débit 24h : ' + (sortieDebit.value ? Number(sortieDebit.value).toLocaleString('fr-FR') + ' m³' : '-'));
        lines.push('  • Photo préleveur : ' + (state.sortiePhoto ? '✓ Capturée' : 'Non jointe'));

        if (ratio) {
          lines.push('');
          lines.push('📊 *SYNTHÈSE VOLUMÉTRIQUE*');
          lines.push('  • Ratio Sortie / Entrée : ' + ratio + ' %');
          if (delta) lines.push('  • Écart : ' + (Number(delta) > 0 ? '+' + delta : delta) + ' m³');
        }

        if (observations.value.trim()) {
          lines.push('');
          lines.push('📝 *Remarques terrain* :');
          lines.push(observations.value.trim());
        }

        lines.push('');
        lines.push('📄 *Rapport PDF officiel avec photos* :');
        lines.push('Fichier généré : ' + (state.lastFileName || 'Bilan_Autosurveillance.pdf'));

        return lines.join('\n');
      }

      // Fonction d'envoi vers WhatsApp
      async function triggerWhatsAppShare() {
        const text = generateReportSummary();
        // Essai Web Share API avec fichier PDF si supporté (sur smartphone Android/iOS)
        if (state.lastBlob && navigator.share && navigator.canShare) {
          try {
            const file = new File([state.lastBlob], state.lastFileName || 'Bilan_Autosurveillance.pdf', { type: 'application/pdf' });
            if (navigator.canShare({ files: [file] })) {
              await navigator.share({
                title: 'Bilan Autosurveillance STEP - ' + nomStep.value,
                text: text,
                files: [file]
              });
              return;
            }
          } catch (e) {
            if (e.name === 'AbortError') return;
          }
        }
        // Fallback standard wa.me
        const url = 'https://wa.me/?text=' + encodeURIComponent(text);
        window.open(url, '_blank', 'noopener,noreferrer');
      }

      // Fonction d'envoi par Email (mailto:)
      function triggerEmailSend() {
        const recipient = (destinataireEmail ? destinataireEmail.value : '').trim();
        const subject = '[Autosurveillance STEP] Bilan 24h - ' + (nomStep.value || 'STEP') + ' (' + (dateAutosurveillance.value || '') + ')';
        const body = 'Bonjour,\n\nVeuillez trouver ci-dessous le bilan d\'autosurveillance 24h pour la station ' + nomStep.value + '.\nLe document PDF officiel haute définition avec photos certifiées (' + (state.lastFileName || 'rapport.pdf') + ') est généré et prêt en pièce jointe.\n\n' + generateReportSummary() + '\n\nCordialement,\n' + (technicienNom.value || 'L\'exploitant de la station');
        
        const mailtoUrl = 'mailto:' + encodeURIComponent(recipient) + '?subject=' + encodeURIComponent(subject) + '&body=' + encodeURIComponent(body);
        const a = document.createElement('a');
        a.href = mailtoUrl;
        a.style.display = 'none';
        document.body.appendChild(a);
        a.click();
        setTimeout(() => document.body.removeChild(a), 150);
      }

      // Soumission du formulaire
      form.addEventListener('submit', async function(e) {
        e.preventDefault();

        if (!validateForm()) return;

        btnSubmit.disabled = true;
        btnText.textContent = "Génération du PDF officiel & photos...";
        btnIconSend.classList.add('hidden');
        btnSpinner.classList.remove('hidden');

        try {
          await new Promise(r => setTimeout(r, 200));

          const pdfRes = await buildPdf();
          state.lastBlob = pdfRes.blob;
          state.lastFileName = pdfRes.fileName;
          state.lastPdfRes = pdfRes;

          // 1. Télécharger directement le PDF sur l'appareil
          downloadFile(pdfRes.blob, pdfRes.fileName);

          // 2. Mettre à jour le panneau d'action de la Section 4
          if (section4SharePanel && section4FileName) {
            section4FileName.textContent = pdfRes.fileName;
            section4SharePanel.classList.remove('hidden');
          }

          // 3. Ouvrir la modale d'aperçu et de partage
          modalFileName.textContent = pdfRes.fileName;
          const modalPdfFrame = document.getElementById('modalPdfFrame');
          if (modalPdfFrame) {
            modalPdfFrame.src = URL.createObjectURL(pdfRes.blob);
          }
          successModal.classList.remove('hidden');

        } catch (err) {
          console.error(err);
          alert("Erreur lors de la génération du rapport : " + err.message);
        } finally {
          btnSubmit.disabled = false;
          btnText.textContent = "Générer le Rapport PDF (Prêt pour WhatsApp & Mail)";
          btnIconSend.classList.remove('hidden');
          btnSpinner.classList.add('hidden');
        }
      });

      // Actions dans la Section 4
      if (section4BtnWhatsApp) {
        section4BtnWhatsApp.addEventListener('click', triggerWhatsAppShare);
      }
      if (section4BtnEmail) {
        section4BtnEmail.addEventListener('click', triggerEmailSend);
      }
      if (section4BtnDownload) {
        section4BtnDownload.addEventListener('click', function() {
          if (state.lastBlob) downloadFile(state.lastBlob, state.lastFileName);
        });
      }

      // Actions dans la Modale
      modalBtnClose.addEventListener('click', function() {
        successModal.classList.add('hidden');
      });
      if (modalBtnBottomClose) {
        modalBtnBottomClose.addEventListener('click', function() {
          successModal.classList.add('hidden');
        });
      }
      modalBtnDownload.addEventListener('click', function() {
        if (state.lastBlob) downloadFile(state.lastBlob, state.lastFileName);
      });
      modalBtnWhatsApp.addEventListener('click', triggerWhatsAppShare);
      modalBtnEmail.addEventListener('click', triggerEmailSend);

      if (modalBtnFooterWhatsApp) {
        modalBtnFooterWhatsApp.addEventListener('click', triggerWhatsAppShare);
      }
      if (modalBtnFooterEmail) {
        modalBtnFooterEmail.addEventListener('click', triggerEmailSend);
      }

      // Copier la synthèse
      if (modalBtnCopy) {
        modalBtnCopy.addEventListener('click', async function() {
          const text = generateReportSummary();
          try {
            await navigator.clipboard.writeText(text);
          } catch (e) {
            const t = document.createElement('textarea');
            t.value = text;
            document.body.appendChild(t);
            t.select();
            document.execCommand('copy');
            document.body.removeChild(t);
          }
          if (modalCopyText) {
            modalCopyText.textContent = 'Copié !';
            setTimeout(() => { modalCopyText.textContent = 'Copier la synthèse'; }, 2000);
          }
        });
      }

      // Bouton Exemple rapide de démonstration
      btnExemple.addEventListener('click', function() {
        nomStep.value = "STEP Val de Loire Métropole (45 000 EH)";
        dateAutosurveillance.value = today;
        technicienNom.value = "Laurent Juillien";
        meteo.value = "Temps sec";
        if (destinataireEmail) destinataireEmail.value = "autosurveillance@grand-bassin.fr";

        entreeDate.value = today;
        entreeHeure.value = "08:15";
        entreeTemperature.value = "3.6";
        entreeDebit.value = "3420.5";

        sortieDate.value = today;
        sortieHeure.value = "08:35";
        sortieTemperature.value = "4.1";
        sortieDebit.value = "3390.2";

        observations.value = "Préleveurs réfrigérés conformes. Absence de colmatage sur les crépines d'aspiration. Échantillons composites clairs en sortie.";

        createSampleImage('PRÉLEVEUR ENTRÉE - EAUX BRUTES', '#0369a1').then(dataUrl => {
          state.entreePhoto = dataUrl;
          entreePreviewImg.src = dataUrl;
          entreePlaceholder.classList.add('hidden');
          entreePreviewContainer.classList.remove('hidden');
          clearError('entreePhoto');
        });

        createSampleImage('PRÉLEVEUR SORTIE - REJET TRAITÉ', '#059669').then(dataUrl => {
          state.sortiePhoto = dataUrl;
          sortiePreviewImg.src = dataUrl;
          sortiePlaceholder.classList.add('hidden');
          sortiePreviewContainer.classList.remove('hidden');
          clearError('sortiePhoto');
        });

        ['nomStep', 'dateAutosurveillance', 'entreeDate', 'entreeHeure', 'entreeTemperature', 'entreeDebit', 'sortieDate', 'sortieHeure', 'sortieTemperature', 'sortieDebit', 'entreePhoto', 'sortiePhoto'].forEach(clearError);
        validationBanner.classList.add('hidden');
      });

      // Générateur d'image d'échantillon pour test
      function createSampleImage(title, accentColor) {
        return new Promise(resolve => {
          const c = document.createElement('canvas');
          c.width = 640;
          c.height = 480;
          const ctx = c.getContext('2d');
          
          ctx.fillStyle = '#1e293b';
          ctx.fillRect(0, 0, 640, 480);
          
          ctx.strokeStyle = '#334155';
          ctx.lineWidth = 1;
          for (let x = 0; x < 640; x += 40) {
            ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, 480); ctx.stroke();
          }
          for (let y = 0; y < 480; y += 40) {
            ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(640, y); ctx.stroke();
          }

          ctx.fillStyle = accentColor;
          ctx.fillRect(120, 90, 400, 300);

          ctx.fillStyle = '#0f172a';
          ctx.fillRect(160, 130, 320, 140);

          ctx.fillStyle = '#38bdf8';
          ctx.font = 'bold 20px monospace';
          ctx.fillText("PRELEVEUR AUTOMATIQUE", 180, 170);
          ctx.fillStyle = '#4ade80';
          ctx.font = 'bold 24px monospace';
          ctx.fillText("TEMP: +3.8°C [CONFORME]", 180, 210);
          ctx.fillStyle = '#fde047';
          ctx.font = 'bold 16px monospace';
          ctx.fillText("CYCLES 24H : 24/24 FLACONS", 180, 245);

          ctx.fillStyle = '#ffffff';
          ctx.font = 'bold 20px sans-serif';
          ctx.textAlign = 'center';
          ctx.fillText(title, 320, 350);

          ctx.fillStyle = '#94a3b8';
          ctx.font = '14px sans-serif';
          ctx.fillText("Contrôle Terrain : " + new Date().toLocaleString('fr-FR'), 320, 440);

          resolve(c.toDataURL('image/jpeg', 0.85));
        });
      }

      // Bouton Reset
      btnReset.addEventListener('click', function() {
        if (confirm("Réinitialiser l'ensemble du formulaire ?")) {
          form.reset();
          state.entreePhoto = null;
          state.sortiePhoto = null;
          state.lastBlob = null;
          state.lastFileName = '';
          entreePreviewContainer.classList.add('hidden');
          entreePlaceholder.classList.remove('hidden');
          sortiePreviewContainer.classList.add('hidden');
          sortiePlaceholder.classList.remove('hidden');
          if (section4SharePanel) section4SharePanel.classList.add('hidden');
          dateAutosurveillance.value = today;
          entreeDate.value = today;
          sortieDate.value = today;
          ['nomStep', 'dateAutosurveillance', 'entreeDate', 'entreeHeure', 'entreeTemperature', 'entreeDebit', 'sortieDate', 'sortieHeure', 'sortieTemperature', 'sortieDebit', 'entreePhoto', 'sortiePhoto'].forEach(clearError);
          validationBanner.classList.add('hidden');
        }
      });

    })();
  </script>
</body>
</html>
