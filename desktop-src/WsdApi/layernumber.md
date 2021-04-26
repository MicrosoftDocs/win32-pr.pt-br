---
description: Define o número da camada de código a ser gerada.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995483"
---
# <a name="layernumber-element"></a><span data-ttu-id="a7501-103">elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="a7501-103">layerNumber element</span></span>

<span data-ttu-id="a7501-104">Define o número da camada de código a ser gerada.</span><span class="sxs-lookup"><span data-stu-id="a7501-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="a7501-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a7501-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="a7501-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7501-106">Attributes</span></span>

<span data-ttu-id="a7501-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="a7501-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a7501-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a7501-108">Child elements</span></span>

<span data-ttu-id="a7501-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a7501-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a7501-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a7501-110">Parent elements</span></span>



| <span data-ttu-id="a7501-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7501-111">Element</span></span>                                     | <span data-ttu-id="a7501-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7501-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7501-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="a7501-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="a7501-114">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a7501-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a7501-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7501-115">Remarks</span></span>

<span data-ttu-id="a7501-116">Os números de camada são usados em tabelas de tempo de execução para distinguir uma camada de código para outra.</span><span class="sxs-lookup"><span data-stu-id="a7501-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="a7501-117">O WSDAPI usa o código gerado que tem um número de camada de 0.</span><span class="sxs-lookup"><span data-stu-id="a7501-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="a7501-118">Normalmente, esse valor será 1, indicando que o código gerado está em camadas na parte superior do WSDAPI e nenhuma outra camada.</span><span class="sxs-lookup"><span data-stu-id="a7501-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="a7501-119">Em alguns casos, números mais altos podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="a7501-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="a7501-120">Por exemplo, se uma empresa produz código para uma classe de dispositivo (camada numerada 1), um fornecedor de hardware específico pode desejar adicionar uma camada 2 de número de camada adicional.</span><span class="sxs-lookup"><span data-stu-id="a7501-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="a7501-121">Os valores válidos, exceto no caso do WSDAPI em si, são maiores que 0 e menores que 16.</span><span class="sxs-lookup"><span data-stu-id="a7501-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="a7501-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a7501-122">Element information</span></span>



| <span data-ttu-id="a7501-123">Label</span><span class="sxs-lookup"><span data-stu-id="a7501-123">Label</span></span> | <span data-ttu-id="a7501-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a7501-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="a7501-125">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7501-125">Minimum supported system</span></span><br/> | <span data-ttu-id="a7501-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7501-126">Windows Vista</span></span> |
| <span data-ttu-id="a7501-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a7501-127">Can be empty</span></span>                        | <span data-ttu-id="a7501-128">Sim</span><span class="sxs-lookup"><span data-stu-id="a7501-128">Yes</span></span>           |



 

 




