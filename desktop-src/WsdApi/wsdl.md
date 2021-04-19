---
description: Especifica um arquivo WSDL para processar informações de contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcb96e063a289e16d5e459b59cb8808a763618a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380730"
---
# <a name="wsdl-element"></a><span data-ttu-id="60e97-103">elemento wsdl</span><span class="sxs-lookup"><span data-stu-id="60e97-103">wsdl element</span></span>

<span data-ttu-id="60e97-104">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="60e97-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="60e97-105">Uso</span><span class="sxs-lookup"><span data-stu-id="60e97-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="60e97-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="60e97-106">Attributes</span></span>

<span data-ttu-id="60e97-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="60e97-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="60e97-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="60e97-108">Child elements</span></span>



| <span data-ttu-id="60e97-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="60e97-109">Element</span></span>                                           | <span data-ttu-id="60e97-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="60e97-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60e97-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="60e97-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="60e97-112">Impede a geração de instruções de importação para destinos especificados nomeados em um \<wsdl:import> elemento em um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="60e97-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="60e97-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="60e97-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="60e97-114">Especifica o local de download para uma \<wsdl:import> diretiva que não especifica explicitamente um local.</span><span class="sxs-lookup"><span data-stu-id="60e97-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="60e97-115">**Multi-Path**</span><span class="sxs-lookup"><span data-stu-id="60e97-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="60e97-116">Arquivo e caminho do arquivo de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="60e97-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="60e97-117">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="60e97-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="60e97-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="60e97-118">Parent elements</span></span>



| <span data-ttu-id="60e97-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="60e97-119">Element</span></span>                                     | <span data-ttu-id="60e97-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="60e97-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="60e97-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="60e97-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="60e97-122">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="60e97-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="60e97-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="60e97-123">Remarks</span></span>

<span data-ttu-id="60e97-124">Todos os elementos [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) que aparecem após o elemento [**Path**](path.md) em um arquivo de configuração XML serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="60e97-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="60e97-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="60e97-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="60e97-126">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60e97-126">Minimum supported system</span></span><br/> | <span data-ttu-id="60e97-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60e97-127">Windows Vista</span></span> |
| <span data-ttu-id="60e97-128">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="60e97-128">Can be empty</span></span>                        | <span data-ttu-id="60e97-129">Não</span><span class="sxs-lookup"><span data-stu-id="60e97-129">No</span></span>            |



 

 




