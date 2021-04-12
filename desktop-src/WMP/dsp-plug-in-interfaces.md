---
title: Interfaces de plug-in do DSP
description: Interfaces de plug-in do DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-ins do Windows Media Player, interfaces DSP
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces DSP
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- plug-ins de processamento de sinal digital, interface ISpecifyPropertyPage
- Plug-ins do DSP, interfaces
- Plug-ins do DSP, interface ISpecifyPropertyPage
- interfaces, plug-ins do DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365733"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="9542a-113">Interfaces de plug-in do DSP</span><span class="sxs-lookup"><span data-stu-id="9542a-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="9542a-114">As interfaces de plug-in do DSP (processamento de sinal digital) são usadas para gerenciar a transferência de dados entre o Windows Media Player e o plug-in.</span><span class="sxs-lookup"><span data-stu-id="9542a-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="9542a-115">Todos os plug-ins DSP podem, opcionalmente, implementar a interface **ISpecifyPropertyPage** para fornecer uma implementação de página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9542a-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="9542a-116">As interfaces a seguir são necessárias para a criação de plug-ins DSP.</span><span class="sxs-lookup"><span data-stu-id="9542a-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="9542a-117">Interface</span><span class="sxs-lookup"><span data-stu-id="9542a-117">Interface</span></span>                                                | <span data-ttu-id="9542a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9542a-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9542a-119">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="9542a-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="9542a-120">Gerencia a troca de dados com o Windows Media Player e executa tarefas de processamento de sinal digital.</span><span class="sxs-lookup"><span data-stu-id="9542a-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="9542a-121">A documentação detalhada está incluída no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="9542a-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="9542a-122">IWMPMediaPluginRegistrar</span><span class="sxs-lookup"><span data-stu-id="9542a-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="9542a-123">Gerencia o registro de plug-in.</span><span class="sxs-lookup"><span data-stu-id="9542a-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="9542a-124">IWMPPlugin</span><span class="sxs-lookup"><span data-stu-id="9542a-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="9542a-125">Gerencia a conexão com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9542a-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="9542a-126">IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="9542a-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="9542a-127">Armazena se o plug-in está habilitado no momento pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9542a-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="9542a-128">IWMPServices</span><span class="sxs-lookup"><span data-stu-id="9542a-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="9542a-129">Recupera informações do Player sobre a hora e o estado do fluxo atuais.</span><span class="sxs-lookup"><span data-stu-id="9542a-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9542a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9542a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9542a-131">**Referência de programação de plug-ins do DSP**</span><span class="sxs-lookup"><span data-stu-id="9542a-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




