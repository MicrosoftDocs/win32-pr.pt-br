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
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104293825"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a><span data-ttu-id="01800-112">Produzindo uma caixa de diálogo para selecionar um tipo específico de formato</span><span class="sxs-lookup"><span data-stu-id="01800-112">Producing a Dialog Box for Selecting a Specific Type of Format</span></span>

<span data-ttu-id="01800-113">Talvez você queira que um aplicativo permita que o usuário selecione um formato de uma lista restrita de formatos em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="01800-113">You might want an application to allow the user to select a format from a restricted list of formats in a dialog box.</span></span> <span data-ttu-id="01800-114">As restrições podem limitar o número de canais, a taxa de amostragem, a marca de formato de onda-áudio ou o número de bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="01800-114">Restrictions might limit the number of channels, the sampling rate, the waveform-audio format tag, or the number of bits per sample.</span></span> <span data-ttu-id="01800-115">Em todos esses casos, você pode gerar a lista usando a função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , definindo os membros **fdwEnum** e **pwfxEnum** da estrutura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="01800-115">In all of these cases, you can generate the list by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, setting the **fdwEnum** and **pwfxEnum** members of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span> <span data-ttu-id="01800-116">O exemplo a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="01800-116">The following example illustrates this process.</span></span>


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



 

 




