---
description: Descreve um namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: elemento nameSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505703"
---
# <a name="namespace-element"></a><span data-ttu-id="0488f-103">elemento nameSpace</span><span class="sxs-lookup"><span data-stu-id="0488f-103">nameSpace element</span></span>

<span data-ttu-id="0488f-104">Descreve um namespace.</span><span class="sxs-lookup"><span data-stu-id="0488f-104">Describes a namespace.</span></span> <span data-ttu-id="0488f-105">Esse namespace pode ser usado para geração de código ou para manipular <as diretivas WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="0488f-105">This namespace may be used for code generation or for handling <wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="0488f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0488f-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="0488f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0488f-107">Attributes</span></span>



| <span data-ttu-id="0488f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="0488f-108">Attribute</span></span>          | <span data-ttu-id="0488f-109">Type</span><span class="sxs-lookup"><span data-stu-id="0488f-109">Type</span></span>                         | <span data-ttu-id="0488f-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0488f-110">Required</span></span>       | <span data-ttu-id="0488f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0488f-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="0488f-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="0488f-112">**uri**</span></span><br/> | <span data-ttu-id="0488f-113">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="0488f-113">character\_string</span></span><br/> | <span data-ttu-id="0488f-114">Yes</span><span class="sxs-lookup"><span data-stu-id="0488f-114">Yes</span></span><br/> | <span data-ttu-id="0488f-115">O URI exclusivo do namespace.</span><span class="sxs-lookup"><span data-stu-id="0488f-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0488f-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0488f-116">Child elements</span></span>



| <span data-ttu-id="0488f-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0488f-117">Element</span></span>                                               | <span data-ttu-id="0488f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0488f-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0488f-119">**Codinome**</span><span class="sxs-lookup"><span data-stu-id="0488f-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="0488f-120">O nome a ser usado para identificar o namespace no código gerado.</span><span class="sxs-lookup"><span data-stu-id="0488f-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="0488f-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="0488f-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="0488f-122">O prefixo a ser usado no código gerado para nomes de macros no namespace.</span><span class="sxs-lookup"><span data-stu-id="0488f-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="0488f-123">**nomes**</span><span class="sxs-lookup"><span data-stu-id="0488f-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="0488f-124">Um nome qualificado no namespace.</span><span class="sxs-lookup"><span data-stu-id="0488f-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="0488f-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="0488f-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="0488f-126">O prefixo ao qual o namespace deve ser mapeado para tornar o XML mais legível.</span><span class="sxs-lookup"><span data-stu-id="0488f-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0488f-127">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="0488f-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="0488f-128">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0488f-128">Parent elements</span></span>



| <span data-ttu-id="0488f-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="0488f-129">Element</span></span>                                     | <span data-ttu-id="0488f-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="0488f-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0488f-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0488f-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0488f-132">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0488f-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0488f-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="0488f-133">Remarks</span></span>

<span data-ttu-id="0488f-134">Esse elemento pode ser usado para fornecer ao gerador de código informações adicionais sobre namespaces que ele encontra em arquivos WSDL e XSD ou para introduzir novos namespaces.</span><span class="sxs-lookup"><span data-stu-id="0488f-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="0488f-135">Os namespaces implícitos por reflexão de tipo ou especificados em arquivos WSDL e XSD são analisados automaticamente pelo gerador de código e não precisam ser definidos explicitamente no script.</span><span class="sxs-lookup"><span data-stu-id="0488f-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="0488f-136">Em alguns casos, esse elemento pode ser usado para adicionar propriedades ou nomes adicionais a um namespace que é referenciado por reflexão de tipo ou WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="0488f-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="0488f-137">O gerador de código não considera isso como um conflito.</span><span class="sxs-lookup"><span data-stu-id="0488f-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="0488f-138">O XML a seguir mostra um elemento de nameSpace (com filhos omitidos para fins de brevidade).</span><span class="sxs-lookup"><span data-stu-id="0488f-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="0488f-139">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0488f-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0488f-140">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0488f-140">Minimum supported system</span></span><br/> | <span data-ttu-id="0488f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0488f-141">Windows Vista</span></span> |
| <span data-ttu-id="0488f-142">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="0488f-142">Can be empty</span></span>                        | <span data-ttu-id="0488f-143">Sim</span><span class="sxs-lookup"><span data-stu-id="0488f-143">Yes</span></span>           |



 

 




