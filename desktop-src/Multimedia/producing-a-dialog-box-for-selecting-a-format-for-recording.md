---
title: Produzindo uma caixa de diálogo para selecionar um formato para gravação
description: Produzindo uma caixa de diálogo para selecionar um formato para gravação
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (Gerenciador de compactação de áudio), caixas de diálogo em produção
- Exemplos do ACM, caixas de diálogo de produção
- produzindo caixas de diálogo
- função acmFormatChoose
- Gerenciador de compactação de áudio (ACM), selecionando o formato para recodificação
- ACM (Gerenciador de compactação de áudio), selecionando o formato para recodificação
- Exemplos do ACM, seleção de formato para recodificação
- selecionando o formato para recodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104365680"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a><span data-ttu-id="5a2f5-112">Produzindo uma caixa de diálogo para selecionar um formato para gravação</span><span class="sxs-lookup"><span data-stu-id="5a2f5-112">Producing a Dialog Box for Selecting a Format for Recording</span></span>

<span data-ttu-id="5a2f5-113">Um aplicativo pode permitir que o usuário selecione um formato para o qual um dispositivo de wave-áudio instalado fornece suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-113">An application can allow the user to select a format for which an installed waveform-audio device provides native support.</span></span> <span data-ttu-id="5a2f5-114">Por exemplo, talvez você queira que um editor de wave-áudio grave novos dados de wave-áudio sem usar um compressor ou descompactador do ACM para fornecer uma camada de conversão.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-114">For example, you might want a waveform-audio editor to record new waveform-audio data without using an ACM compressor or decompressor to provide a translation layer.</span></span> <span data-ttu-id="5a2f5-115">Para fazer isso, use a função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , especificando os \_ sinalizadores de entrada hardware do ACM FORMATENUMF \_ e ACM \_ FORMATENUMF \_ no membro **fdwEnum** da estrutura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="5a2f5-115">To do this, use the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specifying the ACM\_FORMATENUMF\_HARDWARE and ACM\_FORMATENUMF\_INPUT flags in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

 

 




