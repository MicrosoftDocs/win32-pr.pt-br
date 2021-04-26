---
description: Especifica um arquivo WSDL para processar informações de contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef4bc7b76ce22184e4c2f1ceaa2131ef163a26d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994703"
---
# <a name="wsdl-element"></a><span data-ttu-id="51193-103">elemento wsdl</span><span class="sxs-lookup"><span data-stu-id="51193-103">wsdl element</span></span>

<span data-ttu-id="51193-104">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="51193-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="51193-105">Uso</span><span class="sxs-lookup"><span data-stu-id="51193-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="51193-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="51193-106">Attributes</span></span>

<span data-ttu-id="51193-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="51193-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="51193-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="51193-108">Child elements</span></span>



| <span data-ttu-id="51193-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="51193-109">Element</span></span>                                           | <span data-ttu-id="51193-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="51193-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51193-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="51193-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="51193-112">Impede a geração de instruções de importação para destinos especificados nomeados em um \<wsdl:import> elemento em um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="51193-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="51193-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="51193-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="51193-114">Especifica o local de download para uma \<wsdl:import> diretiva que não especifica explicitamente um local.</span><span class="sxs-lookup"><span data-stu-id="51193-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="51193-115">**Multi-Path**</span><span class="sxs-lookup"><span data-stu-id="51193-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="51193-116">Arquivo e caminho do arquivo de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="51193-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="51193-117">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="51193-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="51193-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="51193-118">Parent elements</span></span>



| <span data-ttu-id="51193-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="51193-119">Element</span></span>                                     | <span data-ttu-id="51193-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="51193-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="51193-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="51193-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="51193-122">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="51193-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="51193-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="51193-123">Remarks</span></span>

<span data-ttu-id="51193-124">Todos os elementos [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) que aparecem após o elemento [**Path**](path.md) em um arquivo de configuração XML serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="51193-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="51193-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="51193-125">Element information</span></span>



| <span data-ttu-id="51193-126">Label</span><span class="sxs-lookup"><span data-stu-id="51193-126">Label</span></span> | <span data-ttu-id="51193-127">Valor</span><span class="sxs-lookup"><span data-stu-id="51193-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="51193-128">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51193-128">Minimum supported system</span></span><br/> | <span data-ttu-id="51193-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51193-129">Windows Vista</span></span> |
| <span data-ttu-id="51193-130">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="51193-130">Can be empty</span></span>                        | <span data-ttu-id="51193-131">Não</span><span class="sxs-lookup"><span data-stu-id="51193-131">No</span></span>            |



 

 




