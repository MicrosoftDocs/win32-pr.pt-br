---
description: Inclui o conteúdo de uma macro ou arquivo na saída gerada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: incluir elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995773"
---
# <a name="include-element"></a><span data-ttu-id="a295f-103">incluir elemento</span><span class="sxs-lookup"><span data-stu-id="a295f-103">include element</span></span>

<span data-ttu-id="a295f-104">Inclui o conteúdo de uma macro ou arquivo na saída gerada.</span><span class="sxs-lookup"><span data-stu-id="a295f-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="a295f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a295f-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="a295f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a295f-106">Attributes</span></span>



| <span data-ttu-id="a295f-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="a295f-107">Attribute</span></span>            | <span data-ttu-id="a295f-108">Type</span><span class="sxs-lookup"><span data-stu-id="a295f-108">Type</span></span>                         | <span data-ttu-id="a295f-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a295f-109">Required</span></span>      | <span data-ttu-id="a295f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a295f-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="a295f-111">**file**</span><span class="sxs-lookup"><span data-stu-id="a295f-111">**file**</span></span><br/>  | <span data-ttu-id="a295f-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="a295f-112">character\_string</span></span><br/> | <span data-ttu-id="a295f-113">Não</span><span class="sxs-lookup"><span data-stu-id="a295f-113">No</span></span><br/> | <span data-ttu-id="a295f-114">O caminho para o arquivo a ser incluído.</span><span class="sxs-lookup"><span data-stu-id="a295f-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="a295f-115">**Ela**</span><span class="sxs-lookup"><span data-stu-id="a295f-115">**macro**</span></span><br/> | <span data-ttu-id="a295f-116">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="a295f-116">character\_string</span></span><br/> | <span data-ttu-id="a295f-117">Não</span><span class="sxs-lookup"><span data-stu-id="a295f-117">No</span></span><br/> | <span data-ttu-id="a295f-118">O nome da macro a ser incluída.</span><span class="sxs-lookup"><span data-stu-id="a295f-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="a295f-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a295f-119">Child elements</span></span>

<span data-ttu-id="a295f-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a295f-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a295f-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a295f-121">Parent elements</span></span>



| <span data-ttu-id="a295f-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="a295f-122">Element</span></span>                         | <span data-ttu-id="a295f-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="a295f-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a295f-124">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a295f-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="a295f-125">Direciona o gerador de código para gerar um arquivo e especifica o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="a295f-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a295f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a295f-126">Remarks</span></span>

<span data-ttu-id="a295f-127">O atributo de **macro** ou o atributo de **arquivo** deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a295f-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="a295f-128">Não especifique ambos os atributos.</span><span class="sxs-lookup"><span data-stu-id="a295f-128">Do not specify both attributes.</span></span>

<span data-ttu-id="a295f-129">WsdCodeGen define uma macro chamada **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="a295f-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="a295f-130">Quando essa macro é incluída, o código gerado contém um bloco de comentário de alta visibilidade que instrui os desenvolvedores a não modificar o código gerado.</span><span class="sxs-lookup"><span data-stu-id="a295f-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="a295f-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a295f-131">Examples</span></span>

<span data-ttu-id="a295f-132">O XML a seguir mostra como incluir a macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="a295f-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="a295f-133">Esse XML pode ser adicionado a um arquivo de configuração XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="a295f-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="a295f-134">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a295f-134">Element information</span></span>



| <span data-ttu-id="a295f-135">Label</span><span class="sxs-lookup"><span data-stu-id="a295f-135">Label</span></span> | <span data-ttu-id="a295f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a295f-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="a295f-137">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a295f-137">Minimum supported system</span></span><br/> | <span data-ttu-id="a295f-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a295f-138">Windows Vista</span></span> |
| <span data-ttu-id="a295f-139">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a295f-139">Can be empty</span></span>                        | <span data-ttu-id="a295f-140">Sim</span><span class="sxs-lookup"><span data-stu-id="a295f-140">Yes</span></span>           |



 

 




