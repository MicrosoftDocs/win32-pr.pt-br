---
description: Especifica uma palavra-chave para um provedor de MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763948"
---
# <a name="keyword-element"></a><span data-ttu-id="7680e-103">elemento keyword</span><span class="sxs-lookup"><span data-stu-id="7680e-103">keyword element</span></span>

<span data-ttu-id="7680e-104">Especifica uma palavra-chave para um provedor de [MFTrace](mftrace.md) .</span><span class="sxs-lookup"><span data-stu-id="7680e-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="7680e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7680e-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="7680e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7680e-106">Attributes</span></span>



| <span data-ttu-id="7680e-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="7680e-107">Attribute</span></span>         | <span data-ttu-id="7680e-108">Type</span><span class="sxs-lookup"><span data-stu-id="7680e-108">Type</span></span>             | <span data-ttu-id="7680e-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7680e-109">Required</span></span>       | <span data-ttu-id="7680e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7680e-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="7680e-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="7680e-111">**ID**</span></span><br/> | <span data-ttu-id="7680e-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="7680e-112">CDATA</span></span><br/> | <span data-ttu-id="7680e-113">Yes</span><span class="sxs-lookup"><span data-stu-id="7680e-113">Yes</span></span><br/> | <span data-ttu-id="7680e-114">O nome ou a máscara da palavra-chave</span><span class="sxs-lookup"><span data-stu-id="7680e-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="7680e-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7680e-115">Child elements</span></span>

<span data-ttu-id="7680e-116">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="7680e-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7680e-117">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7680e-117">Parent elements</span></span>



| <span data-ttu-id="7680e-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="7680e-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="7680e-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="7680e-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="7680e-120">**operador**</span><span class="sxs-lookup"><span data-stu-id="7680e-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="7680e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7680e-121">Remarks</span></span>

<span data-ttu-id="7680e-122">Para o elemento [**mfdetours**](mfdetours.md) , as palavras-chave válidas são listadas no tópico [MFTrace Words](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="7680e-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="7680e-123">Para o elemento [**Provider**](provider.md) , as palavras-chave dependem do provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7680e-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="7680e-124">Você pode usar o utilitário Wevtutil.exe para listar as palavras-chave de um determinado provedor.</span><span class="sxs-lookup"><span data-stu-id="7680e-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="7680e-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7680e-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="7680e-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="7680e-126">Can be empty</span></span> | <span data-ttu-id="7680e-127">Yes</span><span class="sxs-lookup"><span data-stu-id="7680e-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="7680e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7680e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7680e-129">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="7680e-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="7680e-130">Palavras-chave MFTrace</span><span class="sxs-lookup"><span data-stu-id="7680e-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




