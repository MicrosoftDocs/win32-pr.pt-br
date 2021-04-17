---
title: Elemento BASE
description: O elemento BASE define uma cadeia de caracteres de URL anexada à frente das URLs enviadas ao Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Elemento BASE Windows Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760894"
---
# <a name="base-element"></a><span data-ttu-id="fe734-104">Elemento BASE</span><span class="sxs-lookup"><span data-stu-id="fe734-104">BASE Element</span></span>

<span data-ttu-id="fe734-105">O elemento **base** define uma cadeia de caracteres de URL anexada à frente das URLs enviadas ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe734-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="fe734-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe734-106">Attributes</span></span>

<span data-ttu-id="fe734-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="fe734-107">**HREF** (required)</span></span>

<span data-ttu-id="fe734-108">A cadeia de caracteres anexada à frente às URLs enviadas ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe734-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="fe734-109">O valor padrão é a cadeia de caracteres nula ("").</span><span class="sxs-lookup"><span data-stu-id="fe734-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fe734-110">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="fe734-110">Parent/Child Elements</span></span>



| <span data-ttu-id="fe734-111">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="fe734-111">Hierarchy</span></span>       | <span data-ttu-id="fe734-112">Elementos</span><span class="sxs-lookup"><span data-stu-id="fe734-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="fe734-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fe734-113">Parent elements</span></span> | <span data-ttu-id="fe734-114">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="fe734-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="fe734-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fe734-115">Child elements</span></span>  | <span data-ttu-id="fe734-116">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fe734-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="fe734-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe734-117">Remarks</span></span>

<span data-ttu-id="fe734-118">Esse elemento define uma cadeia de caracteres de URL anexada à frente das URLs de flip URL enviadas ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe734-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="fe734-119">A inversão de URL é um mecanismo de script que faz com que o Windows Media Player abra uma nova URL em um navegador ou quadro de navegador quando recebe um comando de script.</span><span class="sxs-lookup"><span data-stu-id="fe734-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="fe734-120">O elemento **base** é semelhante a um diretório base para links relativos.</span><span class="sxs-lookup"><span data-stu-id="fe734-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="fe734-121">Ele afeta apenas as URLs enviadas usando comandos de script como parte do fluxo de conteúdo que está sendo executado no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe734-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="fe734-122">Um elemento **base** definido como o filho de um elemento **ASX** torna-se o padrão para todo o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="fe734-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="fe734-123">Um elemento **base** definido em um elemento de **entrada** substitui qualquer elemento **base** no elemento pai **ASX** (somente para esse elemento de **entrada** ).</span><span class="sxs-lookup"><span data-stu-id="fe734-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="fe734-124">Se o atributo **href** não terminar com um caractere/, o Windows Media Player acrescentará um ao final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fe734-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fe734-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe734-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="fe734-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe734-126">Requirements</span></span>



| <span data-ttu-id="fe734-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe734-127">Requirement</span></span> | <span data-ttu-id="fe734-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fe734-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fe734-129">Versão</span><span class="sxs-lookup"><span data-stu-id="fe734-129">Version</span></span><br/> | <span data-ttu-id="fe734-130">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fe734-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe734-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe734-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe734-132">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fe734-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="fe734-133">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fe734-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





