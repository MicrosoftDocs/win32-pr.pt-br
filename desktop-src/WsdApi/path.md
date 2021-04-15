---
description: Especifica o local e o nome do arquivo WSDL. O caminho pode ser um caminho absoluto ou relativo para o arquivo, mas não deve ser uma URL.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: elemento Path (serviços Web em dispositivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763ad1479c20553fb7e62ab29e504d56bfa6d950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761296"
---
# <a name="path-element"></a><span data-ttu-id="3548b-104">elemento Path</span><span class="sxs-lookup"><span data-stu-id="3548b-104">path element</span></span>

<span data-ttu-id="3548b-105">Especifica o local e o nome do arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="3548b-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="3548b-106">O caminho pode ser um caminho absoluto ou relativo para o arquivo, mas não deve ser uma URL.</span><span class="sxs-lookup"><span data-stu-id="3548b-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="3548b-107">Uso</span><span class="sxs-lookup"><span data-stu-id="3548b-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="3548b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3548b-108">Attributes</span></span>

<span data-ttu-id="3548b-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="3548b-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3548b-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3548b-110">Child elements</span></span>

<span data-ttu-id="3548b-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="3548b-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3548b-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3548b-112">Parent elements</span></span>



| <span data-ttu-id="3548b-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="3548b-113">Element</span></span>                         | <span data-ttu-id="3548b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3548b-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="3548b-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="3548b-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="3548b-116">Um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="3548b-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="3548b-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3548b-117">Examples</span></span>

<span data-ttu-id="3548b-118">O XML a seguir mostra um elemento **path** válido.</span><span class="sxs-lookup"><span data-stu-id="3548b-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="3548b-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3548b-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="3548b-120">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3548b-120">Minimum supported system</span></span><br/> | <span data-ttu-id="3548b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3548b-121">Windows Vista</span></span> |
| <span data-ttu-id="3548b-122">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="3548b-122">Can be empty</span></span>                        | <span data-ttu-id="3548b-123">Sim</span><span class="sxs-lookup"><span data-stu-id="3548b-123">Yes</span></span>           |



 

 




