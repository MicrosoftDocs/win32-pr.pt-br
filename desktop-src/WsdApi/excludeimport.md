---
description: 'Impede a geração de instruções de importação para destinos especificados nomeados em um elemento wsdl: Import em um arquivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380770"
---
# <a name="excludeimport-element"></a><span data-ttu-id="92faa-103">elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="92faa-103">excludeImport element</span></span>

<span data-ttu-id="92faa-104">Impede a geração de instruções de importação para destinos especificados nomeados em um \<wsdl:import> elemento em um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="92faa-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="92faa-105">Isso pode ser usado para impedir que o WsdCodeGen importe destinos conhecidos, como as especificações de WS-Addressing e WS-Eventing, embora esses destinos sejam referenciados no WSDL.</span><span class="sxs-lookup"><span data-stu-id="92faa-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="92faa-106">O valor desse elemento deve ser definido como o namespace nomeado no \<wsdl:import> elemento a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="92faa-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="92faa-107">Uso</span><span class="sxs-lookup"><span data-stu-id="92faa-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="92faa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="92faa-108">Attributes</span></span>

<span data-ttu-id="92faa-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="92faa-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="92faa-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="92faa-110">Child elements</span></span>

<span data-ttu-id="92faa-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="92faa-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="92faa-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="92faa-112">Parent elements</span></span>



| <span data-ttu-id="92faa-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="92faa-113">Element</span></span>                         | <span data-ttu-id="92faa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="92faa-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="92faa-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="92faa-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="92faa-116">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="92faa-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="92faa-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="92faa-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="92faa-118">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92faa-118">Minimum supported system</span></span><br/> | <span data-ttu-id="92faa-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92faa-119">Windows Vista</span></span> |
| <span data-ttu-id="92faa-120">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="92faa-120">Can be empty</span></span>                        | <span data-ttu-id="92faa-121">Sim</span><span class="sxs-lookup"><span data-stu-id="92faa-121">Yes</span></span>           |



 

 




