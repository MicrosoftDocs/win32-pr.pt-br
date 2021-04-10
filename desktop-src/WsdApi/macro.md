---
description: Define o texto ou CDATA a ser reutilizado pelo elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169798"
---
# <a name="macro-element"></a><span data-ttu-id="0e209-103">elemento macro</span><span class="sxs-lookup"><span data-stu-id="0e209-103">macro element</span></span>

<span data-ttu-id="0e209-104">Define o texto ou CDATA a ser reutilizado pelo elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="0e209-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="0e209-105">Uso</span><span class="sxs-lookup"><span data-stu-id="0e209-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="0e209-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e209-106">Attributes</span></span>



| <span data-ttu-id="0e209-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="0e209-107">Attribute</span></span>           | <span data-ttu-id="0e209-108">Type</span><span class="sxs-lookup"><span data-stu-id="0e209-108">Type</span></span>                         | <span data-ttu-id="0e209-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e209-109">Required</span></span>       | <span data-ttu-id="0e209-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e209-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="0e209-111">**name**</span><span class="sxs-lookup"><span data-stu-id="0e209-111">**name**</span></span><br/> | <span data-ttu-id="0e209-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="0e209-112">character\_string</span></span><br/> | <span data-ttu-id="0e209-113">Yes</span><span class="sxs-lookup"><span data-stu-id="0e209-113">Yes</span></span><br/> | <span data-ttu-id="0e209-114">O nome da macro.</span><span class="sxs-lookup"><span data-stu-id="0e209-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0e209-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0e209-115">Child elements</span></span>

<span data-ttu-id="0e209-116">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="0e209-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0e209-117">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0e209-117">Parent elements</span></span>



| <span data-ttu-id="0e209-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e209-118">Element</span></span>                                     | <span data-ttu-id="0e209-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e209-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e209-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0e209-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0e209-121">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0e209-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0e209-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e209-122">Remarks</span></span>

<span data-ttu-id="0e209-123">WsdCodeGen define uma macro chamada **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="0e209-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="0e209-124">Quando essa macro é incluída, o código gerado contém um bloco de comentário de alta visibilidade que instrui os desenvolvedores a não modificar o código gerado.</span><span class="sxs-lookup"><span data-stu-id="0e209-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="0e209-125">O XML a seguir mostra como incluir a macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="0e209-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="0e209-126">Esse XML pode ser adicionado a um arquivo de configuração XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="0e209-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="0e209-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e209-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0e209-128">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e209-128">Minimum supported system</span></span><br/> | <span data-ttu-id="0e209-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e209-129">Windows Vista</span></span> |
| <span data-ttu-id="0e209-130">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="0e209-130">Can be empty</span></span>                        | <span data-ttu-id="0e209-131">Sim</span><span class="sxs-lookup"><span data-stu-id="0e209-131">Yes</span></span>           |



 

 




