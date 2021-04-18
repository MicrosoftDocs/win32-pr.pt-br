---
title: Evento external. OnChangeViewError
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Evento external. OnChangeViewError do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789543"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="f16b4-105">Evento external. OnChangeViewError</span><span class="sxs-lookup"><span data-stu-id="f16b4-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="f16b4-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="f16b4-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f16b4-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="f16b4-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f16b4-108">O evento **OnChangeViewError** ocorre quando uma chamada para o método [external. changeView](external-changeview.md) resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="f16b4-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="f16b4-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f16b4-109">Possible Values</span></span>

<span data-ttu-id="f16b4-110">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="f16b4-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="f16b4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f16b4-111">Parameters</span></span>

<span data-ttu-id="f16b4-112">A função que manipula esse evento tem os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f16b4-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="f16b4-113"><span id="hr"></span><span id="HR"></span>*Human*</span><span class="sxs-lookup"><span data-stu-id="f16b4-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="f16b4-114">Um código de falha **HRESULT** que indica o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="f16b4-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="f16b4-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="f16b4-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="f16b4-116">A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationType** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="f16b4-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f16b4-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="f16b4-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="f16b4-118">A mesma cadeia de caracteres thatwas passada no parâmetro **LibraryLocationID** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="f16b4-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f16b4-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Sem*</span><span class="sxs-lookup"><span data-stu-id="f16b4-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="f16b4-120">A mesma cadeia de caracteres que foi passada no parâmetro de **filtro** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="f16b4-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f16b4-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span><span class="sxs-lookup"><span data-stu-id="f16b4-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="f16b4-122">A mesma cadeia de caracteres que foi passada no parâmetro **ViewParams** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="f16b4-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f16b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16b4-123">Requirements</span></span>



| <span data-ttu-id="f16b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16b4-124">Requirement</span></span> | <span data-ttu-id="f16b4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f16b4-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f16b4-126">Versão</span><span class="sxs-lookup"><span data-stu-id="f16b4-126">Version</span></span><br/> | <span data-ttu-id="f16b4-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="f16b4-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="f16b4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f16b4-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f16b4-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f16b4-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16b4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f16b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16b4-131">**Externalobject para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f16b4-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





