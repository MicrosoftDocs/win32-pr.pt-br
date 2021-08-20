---
title: Produzindo uma caixa de diálogo para selecionar um filtro
description: Produzindo uma caixa de diálogo para selecionar um filtro
ms.assetid: 4cbb9276-6ce6-4cf4-a000-2b4f9ac42b31
keywords:
- gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (gerenciador de compactação de áudio), produzindo caixas de diálogo
- Exemplos do ACM, produzindo caixas de diálogo
- produzindo caixas de diálogo
- Função acmFilterChoose
- gerenciador de compactação de áudio (ACM), selecionando filtros
- ACM (gerenciador de compactação de áudio), selecionando filtros
- Exemplos do ACM, selecionando filtros
- selecionando filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70015f7e546337983725ae85c683acf5e9b75423e0de0734de4e1293480933ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136600"
---
# <a name="producing-a-dialog-box-for-selecting-a-filter"></a>Produzindo uma caixa de diálogo para selecionar um filtro

Um aplicativo pode permitir que os usuários selecionem uma operação de filtro arbitrária e apliquem-na a dados waveform-audio. No exemplo a seguir, o aplicativo aloca um buffer para manter o filtro e, em seguida, usa a [**função acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) para selecionar o filtro. As funções neste exemplo devem ser chamadas com a marca de filtro ou filtro apropriada.


```C++
MMRESULT        mmr; 
ACMFILTERCHOOSE afc; 
PWAVEFILTER     pwfltr; 
DWORD           cbwfltr; 
 
// Determine the maximum size required for any valid filter 
// for which the ACM has a driver installed and enabled. 
mmr = acmMetrics(NULL, ACM_METRIC_MAX_SIZE_FILTER, &cbwfltr); 
if (MMSYSERR_NOERROR != mmr) { 
 
    // The ACM probably has no drivers installed and 
    // enabled for filter operations. 
    return (mmr); 
} 
 
// Dynamically allocate a structure large enough to hold the 
// maximum sized filter enabled in the system. 
pwfltr = (PWAVEFILTER)LocalAlloc(LPTR, (UINT)cbwfltr); 
if (NULL == pwfltr) { 
    return (MMSYSERR_NOMEM); 
} 
 
// Initialize the ACMFILTERCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfltr      = pwfltr;           // wfltr to receive selection 
afc.cbwfltr     = cbwfltr;          // size of wfltr buffer 
afc.pszTitle    = TEXT("Any Filter Selection"); 
 
// Call the ACM to bring up the filter-selection dialog box. 
mmr = acmFilterChoose(&afc); 
if (MMSYSERR_NOERROR == mmr) { 
    // The user selected a valid filter. The pwfltr buffer, 
    // allocated above, contains the complete filter description. 
} 
 
// Clean up and exit. 
LocalFree((HLOCAL)pwfltr); 
return (mmr); 
 
```



 

 




