---
description: 'Impede a geração de instruções de importação para destinos especificados nomeados em um elemento <WSDL: Import> em um arquivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827829"
---
# <a name="excludeimport-element"></a><span data-ttu-id="f69b9-103">elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="f69b9-103">excludeImport element</span></span>

<span data-ttu-id="f69b9-104">Impede a geração de instruções de importação para destinos especificados nomeados em um elemento <WSDL: Import> em um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="f69b9-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="f69b9-105">Isso pode ser usado para impedir que o WsdCodeGen importe destinos conhecidos, como as especificações de WS-Addressing e WS-Eventing, embora esses destinos sejam referenciados no WSDL.</span><span class="sxs-lookup"><span data-stu-id="f69b9-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="f69b9-106">O valor desse elemento deve ser definido como o namespace nomeado no elemento <WSDL: Import> a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f69b9-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="f69b9-107">Uso</span><span class="sxs-lookup"><span data-stu-id="f69b9-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="f69b9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f69b9-108">Attributes</span></span>

<span data-ttu-id="f69b9-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f69b9-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f69b9-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f69b9-110">Child elements</span></span>

<span data-ttu-id="f69b9-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="f69b9-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f69b9-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f69b9-112">Parent elements</span></span>



| <span data-ttu-id="f69b9-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="f69b9-113">Element</span></span>                         | <span data-ttu-id="f69b9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f69b9-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f69b9-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="f69b9-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="f69b9-116">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="f69b9-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="f69b9-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f69b9-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f69b9-118">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f69b9-118">Minimum supported system</span></span><br/> | <span data-ttu-id="f69b9-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f69b9-119">Windows Vista</span></span> |
| <span data-ttu-id="f69b9-120">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="f69b9-120">Can be empty</span></span>                        | <span data-ttu-id="f69b9-121">Sim</span><span class="sxs-lookup"><span data-stu-id="f69b9-121">Yes</span></span>           |



 

 




