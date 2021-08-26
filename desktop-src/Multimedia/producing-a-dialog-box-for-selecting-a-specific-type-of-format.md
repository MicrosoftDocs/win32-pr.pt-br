---
title: Produzindo uma caixa de diálogo para selecionar um tipo específico de formato
description: Produzindo uma caixa de diálogo para selecionar um tipo específico de formato
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (Gerenciador de compactação de áudio), caixas de diálogo em produção
- Exemplos do ACM, caixas de diálogo de produção
- produzindo caixas de diálogo
- função acmFormatChoose
- Gerenciador de compactação de áudio (ACM), selecionando tipos de formato
- ACM (Gerenciador de compactação de áudio), selecionando tipos de formato
- Exemplos do ACM, seleção de tipos de formato
- Selecionando tipos de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037646"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Produzindo uma caixa de diálogo para selecionar um tipo específico de formato

Talvez você queira que um aplicativo permita que o usuário selecione um formato de uma lista restrita de formatos em uma caixa de diálogo. As restrições podem limitar o número de canais, a taxa de amostragem, a marca de formato de onda-áudio ou o número de bits por amostra. Em todos esses casos, você pode gerar a lista usando a função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , definindo os membros **fdwEnum** e **pwfxEnum** da estrutura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) . O exemplo a seguir ilustra esse processo.


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




