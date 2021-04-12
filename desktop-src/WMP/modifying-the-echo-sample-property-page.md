---
title: Modificando a página de propriedades de exemplo de eco
description: Modificando a página de propriedades de exemplo de eco
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363876"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="68cfe-108">Modificando a página de propriedades de exemplo de eco</span><span class="sxs-lookup"><span data-stu-id="68cfe-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="68cfe-109">A implementação da página de propriedades padrão fornecida pelo exemplo de plug-in DSP do assistente de plug-in do Windows Media Player contém um único controle de caixa de edição que recebe o fator de escala do usuário.</span><span class="sxs-lookup"><span data-stu-id="68cfe-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="68cfe-110">Você precisa modificar a página de propriedades para receber os dois valores de propriedade usados pelo exemplo de eco.</span><span class="sxs-lookup"><span data-stu-id="68cfe-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="68cfe-111">Para obter uma visão geral das páginas de propriedades de plug-in do DSP, consulte [implementando um plug-in do DSP de áudio](implementing-an-audio-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="68cfe-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="68cfe-112">As seções a seguir o orientarão no processo de modificação da página de propriedades de exemplo:</span><span class="sxs-lookup"><span data-stu-id="68cfe-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="68cfe-113">Modificando o recurso de diálogo de eco</span><span class="sxs-lookup"><span data-stu-id="68cfe-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="68cfe-114">Adicionando e modificando os eventos</span><span class="sxs-lookup"><span data-stu-id="68cfe-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="68cfe-115">Como a amostra de eco persiste os dados</span><span class="sxs-lookup"><span data-stu-id="68cfe-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="68cfe-116">Implementando CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="68cfe-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="68cfe-117">Implementando CEchoPropPage:: apply</span><span class="sxs-lookup"><span data-stu-id="68cfe-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="68cfe-118">Implementando CEcho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="68cfe-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="68cfe-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68cfe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68cfe-120">**O exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="68cfe-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




