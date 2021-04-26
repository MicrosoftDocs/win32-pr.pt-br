---
description: Define o prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: elemento layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994692"
---
# <a name="layerprefix-element"></a><span data-ttu-id="54269-103">elemento layerPrefix</span><span class="sxs-lookup"><span data-stu-id="54269-103">layerPrefix element</span></span>

<span data-ttu-id="54269-104">Define o prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados.</span><span class="sxs-lookup"><span data-stu-id="54269-104">Defines the prefix to use in the generated code to assure uniqueness of generated symbols.</span></span>

## <a name="usage"></a><span data-ttu-id="54269-105">Uso</span><span class="sxs-lookup"><span data-stu-id="54269-105">Usage</span></span>

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="54269-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="54269-106">Attributes</span></span>

<span data-ttu-id="54269-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="54269-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="54269-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="54269-108">Child elements</span></span>

<span data-ttu-id="54269-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="54269-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="54269-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="54269-110">Parent elements</span></span>



| <span data-ttu-id="54269-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="54269-111">Element</span></span>                                     | <span data-ttu-id="54269-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="54269-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="54269-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="54269-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="54269-114">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="54269-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="54269-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="54269-115">Remarks</span></span>

<span data-ttu-id="54269-116">Cada script do gerador de código deve definir uma cadeia de caracteres de prefixo exclusiva para os módulos criados.</span><span class="sxs-lookup"><span data-stu-id="54269-116">Each code generator script should define a unique prefix string for the modules created.</span></span> <span data-ttu-id="54269-117">Por exemplo, os scripts de quadro de imagem usam um prefixo de "PFDEMO".</span><span class="sxs-lookup"><span data-stu-id="54269-117">For example, the Picture Frame scripts use a prefix of "PFDEMO".</span></span>

<span data-ttu-id="54269-118">O WSDAPI usa o prefixo "WSD".</span><span class="sxs-lookup"><span data-stu-id="54269-118">WSDAPI uses the prefix "WSD".</span></span>

## <a name="element-information"></a><span data-ttu-id="54269-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="54269-119">Element information</span></span>



| <span data-ttu-id="54269-120">Label</span><span class="sxs-lookup"><span data-stu-id="54269-120">Label</span></span> | <span data-ttu-id="54269-121">Valor</span><span class="sxs-lookup"><span data-stu-id="54269-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="54269-122">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54269-122">Minimum supported system</span></span><br/> | <span data-ttu-id="54269-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54269-123">Windows Vista</span></span> |
| <span data-ttu-id="54269-124">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="54269-124">Can be empty</span></span>                        | <span data-ttu-id="54269-125">Sim</span><span class="sxs-lookup"><span data-stu-id="54269-125">Yes</span></span>           |



 

 




