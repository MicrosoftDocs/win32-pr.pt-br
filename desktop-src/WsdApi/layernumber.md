---
description: Define o número da camada de código a ser gerada.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169799"
---
# <a name="layernumber-element"></a><span data-ttu-id="a9a90-103">elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="a9a90-103">layerNumber element</span></span>

<span data-ttu-id="a9a90-104">Define o número da camada de código a ser gerada.</span><span class="sxs-lookup"><span data-stu-id="a9a90-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="a9a90-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a9a90-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="a9a90-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9a90-106">Attributes</span></span>

<span data-ttu-id="a9a90-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="a9a90-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a9a90-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a9a90-108">Child elements</span></span>

<span data-ttu-id="a9a90-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a9a90-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a9a90-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a9a90-110">Parent elements</span></span>



| <span data-ttu-id="a9a90-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9a90-111">Element</span></span>                                     | <span data-ttu-id="a9a90-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9a90-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9a90-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="a9a90-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="a9a90-114">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a9a90-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a9a90-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9a90-115">Remarks</span></span>

<span data-ttu-id="a9a90-116">Os números de camada são usados em tabelas de tempo de execução para distinguir uma camada de código para outra.</span><span class="sxs-lookup"><span data-stu-id="a9a90-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="a9a90-117">O WSDAPI usa o código gerado que tem um número de camada de 0.</span><span class="sxs-lookup"><span data-stu-id="a9a90-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="a9a90-118">Normalmente, esse valor será 1, indicando que o código gerado está em camadas na parte superior do WSDAPI e nenhuma outra camada.</span><span class="sxs-lookup"><span data-stu-id="a9a90-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="a9a90-119">Em alguns casos, números mais altos podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="a9a90-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="a9a90-120">Por exemplo, se uma empresa produz código para uma classe de dispositivo (camada numerada 1), um fornecedor de hardware específico pode desejar adicionar uma camada 2 de número de camada adicional.</span><span class="sxs-lookup"><span data-stu-id="a9a90-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="a9a90-121">Os valores válidos, exceto no caso do WSDAPI em si, são maiores que 0 e menores que 16.</span><span class="sxs-lookup"><span data-stu-id="a9a90-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="a9a90-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a9a90-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a9a90-123">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a90-123">Minimum supported system</span></span><br/> | <span data-ttu-id="a9a90-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9a90-124">Windows Vista</span></span> |
| <span data-ttu-id="a9a90-125">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a9a90-125">Can be empty</span></span>                        | <span data-ttu-id="a9a90-126">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a90-126">Yes</span></span>           |



 

 




