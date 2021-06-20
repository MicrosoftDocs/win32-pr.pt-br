---
description: Saiba mais sobre como referenciar parâmetros e o elemento ParameterDef. Um exemplo de uma Opção que inclui um elemento ParameterRef é a Opção de tamanho de mídia personalizada.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Parâmetros de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405319"
---
# <a name="referencing-parameters"></a><span data-ttu-id="d11da-104">Parâmetros de referência</span><span class="sxs-lookup"><span data-stu-id="d11da-104">Referencing Parameters</span></span>

<span data-ttu-id="d11da-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d11da-105">This topic is not current.</span></span> <span data-ttu-id="d11da-106">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d11da-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d11da-107">Um exemplo concreto de uma Opção que inclui um elemento ParameterRef é a Opção de tamanho de mídia personalizada.</span><span class="sxs-lookup"><span data-stu-id="d11da-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="d11da-108">Observe que ele faz referência a dois parâmetros: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="d11da-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="d11da-109">Cada instância ParameterRef refere-se a uma instância ParameterDef definida em outro lugar no documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d11da-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="d11da-110">Para obter informações sobre o elemento ParameterDef, consulte [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="d11da-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="d11da-111">Para obter informações conceituais sobre como definir parâmetros, consulte [ParameterDef e ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="d11da-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="d11da-112">Simplesmente criar uma Opção parametrizada não é suficiente para garantir que a Opção seja tratada e processada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d11da-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="d11da-113">O provedor e os clientes PrintCapabilities/PrintTicket devem fornecer suporte adicional para implementar corretamente instâncias de Opção parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="d11da-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="d11da-114">Os comportamentos necessários são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d11da-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d11da-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d11da-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d11da-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d11da-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



