---
title: Produzindo uma caixa de diálogo para selecionar um formato para salvar
description: Produzindo uma caixa de diálogo para selecionar um formato para salvar
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (Gerenciador de compactação de áudio), caixas de diálogo em produção
- Exemplos do ACM, caixas de diálogo de produção
- produzindo caixas de diálogo
- função acmFormatChoose
- Gerenciador de compactação de áudio (ACM), selecionando o formato para salvar
- ACM (Gerenciador de compactação de áudio), selecionando o formato para salvar
- Exemplos do ACM, selecionando o formato para salvar
- selecionando o formato para salvar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104365681"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="c6174-112">Produzindo uma caixa de diálogo para selecionar um formato para salvar</span><span class="sxs-lookup"><span data-stu-id="c6174-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="c6174-113">Talvez você queira que um aplicativo salve dados de formato de onda e áudio existentes em outro formato.</span><span class="sxs-lookup"><span data-stu-id="c6174-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="c6174-114">Por exemplo, um editor de wave-áudio pode salvar um arquivo de wave-áudio como um arquivo compactado.</span><span class="sxs-lookup"><span data-stu-id="c6174-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="c6174-115">Para listar apenas os formatos de destino sugeridos para um formato de origem especificado na caixa de diálogo criada pela função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , especifique o formato de origem no membro **pwfxEnum** e o sinalizador de sugestão de FORMATENUMF do ACM \_ \_ no membro **fdwEnum** da estrutura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="c6174-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="c6174-116">Da mesma forma, para listar formatos de destino válidos para um formato especificado, use o sinalizador de conversão do ACM \_ FORMATENUMF \_ em vez do sinalizador de sugestão de FORMATENUMF do ACM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c6174-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




