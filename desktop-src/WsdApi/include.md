---
description: Inclui o conteúdo de uma macro ou arquivo na saída gerada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: incluir elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011439"
---
# <a name="include-element"></a><span data-ttu-id="c2d72-103">incluir elemento</span><span class="sxs-lookup"><span data-stu-id="c2d72-103">include element</span></span>

<span data-ttu-id="c2d72-104">Inclui o conteúdo de uma macro ou arquivo na saída gerada.</span><span class="sxs-lookup"><span data-stu-id="c2d72-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="c2d72-105">Uso</span><span class="sxs-lookup"><span data-stu-id="c2d72-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="c2d72-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2d72-106">Attributes</span></span>



| <span data-ttu-id="c2d72-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2d72-107">Attribute</span></span>            | <span data-ttu-id="c2d72-108">Type</span><span class="sxs-lookup"><span data-stu-id="c2d72-108">Type</span></span>                         | <span data-ttu-id="c2d72-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c2d72-109">Required</span></span>      | <span data-ttu-id="c2d72-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2d72-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="c2d72-111">**file**</span><span class="sxs-lookup"><span data-stu-id="c2d72-111">**file**</span></span><br/>  | <span data-ttu-id="c2d72-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="c2d72-112">character\_string</span></span><br/> | <span data-ttu-id="c2d72-113">No</span><span class="sxs-lookup"><span data-stu-id="c2d72-113">No</span></span><br/> | <span data-ttu-id="c2d72-114">O caminho para o arquivo a ser incluído.</span><span class="sxs-lookup"><span data-stu-id="c2d72-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="c2d72-115">**Ela**</span><span class="sxs-lookup"><span data-stu-id="c2d72-115">**macro**</span></span><br/> | <span data-ttu-id="c2d72-116">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="c2d72-116">character\_string</span></span><br/> | <span data-ttu-id="c2d72-117">No</span><span class="sxs-lookup"><span data-stu-id="c2d72-117">No</span></span><br/> | <span data-ttu-id="c2d72-118">O nome da macro a ser incluída.</span><span class="sxs-lookup"><span data-stu-id="c2d72-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c2d72-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c2d72-119">Child elements</span></span>

<span data-ttu-id="c2d72-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="c2d72-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c2d72-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c2d72-121">Parent elements</span></span>



| <span data-ttu-id="c2d72-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2d72-122">Element</span></span>                         | <span data-ttu-id="c2d72-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2d72-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2d72-124">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="c2d72-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c2d72-125">Direciona o gerador de código para gerar um arquivo e especifica o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="c2d72-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c2d72-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2d72-126">Remarks</span></span>

<span data-ttu-id="c2d72-127">O atributo de **macro** ou o atributo de **arquivo** deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c2d72-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="c2d72-128">Não especifique ambos os atributos.</span><span class="sxs-lookup"><span data-stu-id="c2d72-128">Do not specify both attributes.</span></span>

<span data-ttu-id="c2d72-129">WsdCodeGen define uma macro chamada **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="c2d72-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="c2d72-130">Quando essa macro é incluída, o código gerado contém um bloco de comentário de alta visibilidade que instrui os desenvolvedores a não modificar o código gerado.</span><span class="sxs-lookup"><span data-stu-id="c2d72-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="c2d72-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2d72-131">Examples</span></span>

<span data-ttu-id="c2d72-132">O XML a seguir mostra como incluir a macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="c2d72-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="c2d72-133">Esse XML pode ser adicionado a um arquivo de configuração XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="c2d72-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="c2d72-134">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c2d72-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c2d72-135">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2d72-135">Minimum supported system</span></span><br/> | <span data-ttu-id="c2d72-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2d72-136">Windows Vista</span></span> |
| <span data-ttu-id="c2d72-137">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="c2d72-137">Can be empty</span></span>                        | <span data-ttu-id="c2d72-138">Sim</span><span class="sxs-lookup"><span data-stu-id="c2d72-138">Yes</span></span>           |



 

 




