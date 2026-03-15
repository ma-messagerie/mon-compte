<?php
/**
 * SmartLink Simplifié - Redirection pondérée avec email
 */

// ============================================================
// 1. CONFIGURATION DES OFFRES
// ============================================================

// Structure: [URL, Poids (plus élevé = plus de chances)]
$offres = [
    // Exemples - modifie selon tes besoins
    ['url' => 'https://www.ever-trck.com/21NCZPT/2CTPL/?uid=45&sub1=%EMAIL%', 'poids' => 5],
    ['url' => 'https://www.ever-trck.com/21NCZPT/9B9DM/?uid=43&sub1=%EMAIL%', 'poids' => 5],
    ['url' => 'https://www.ever-trck.com/21NCZPT/FGXLG/?uid=62&sub1=%EMAIL%', 'poids' => 5],
    ['url' => 'https://www.meilleurrdv.fr/voir-profil/?src=tmii1&pf_email=%EMAIL%', 'poids' => 50],
    ['url' => 'https://ab.pdtrcksus.com/v1/redirect/35449?utm_term=ac&email=%EMAIL%', 'poids' => 1],
    ['url' => 'https://rencontrespouradultes.com/lead/noredir?cid=34870&email=%EMAIL%', 'poids' => 1],
];

// ============================================================
// 2. FONCTIONS
// ============================================================

/**
 * Sélectionne une offre de manière pondérée
 */
function selectionnerOffrePonderee($offres) {
    $totalPoids = array_sum(array_column($offres, 'poids'));
    $random = mt_rand(1, $totalPoids);

    $cumul = 0;
    foreach ($offres as $offre) {
        $cumul += $offre['poids'];
        if ($random <= $cumul) {
            return $offre['url'];
        }
    }

    // Fallback (ne devrait jamais arriver)
    return $offres[0]['url'];
}

/**
 * Remplace %EMAIL% par la valeur du paramètre
 */
function preparerUrl($url, $email) {
    return str_replace('%EMAIL%', rawurlencode($email), $url);
}

// ============================================================
// 3. EXÉCUTION
// ============================================================

// Récupérer l'email depuis l'URL (?u=email@example.com)
$email = $_GET['u'] ?? $_POST['u'] ?? '';

// Sélectionner une offre pondérée
$urlChoisie = selectionnerOffrePonderee($offres);

// Remplacer %EMAIL%
$urlFinale = preparerUrl($urlChoisie, $email);

// Redirection
header("Location: $urlFinale");
exit;
