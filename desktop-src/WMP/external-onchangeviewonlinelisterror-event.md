---
title: Evento external. OnChangeViewOnlineListError
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Evento external. OnChangeViewOnlineListError do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789542"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="5a44d-105">Evento external. OnChangeViewOnlineListError</span><span class="sxs-lookup"><span data-stu-id="5a44d-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="5a44d-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5a44d-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5a44d-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5a44d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5a44d-108">O evento **OnChangeViewOnlineListError** ocorre quando uma chamada para o método [external. changeViewOnlineList](external-changeviewonlinelist.md) resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="5a44d-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="5a44d-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5a44d-109">Possible Values</span></span>

<span data-ttu-id="5a44d-110">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="5a44d-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a44d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a44d-111">Parameters</span></span>

<span data-ttu-id="5a44d-112">A função que manipula esse erro tem os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a44d-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="5a44d-113"><span id="hr"></span><span id="HR"></span>*Human*</span><span class="sxs-lookup"><span data-stu-id="5a44d-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-114">Um código de falha **HRESULT** que indica o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="5a44d-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="5a44d-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-116">A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="5a44d-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-118">A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationID** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="5a44d-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-120">A mesma cadeia de caracteres que foi passada no parâmetro **params** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="5a44d-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-122">A mesma cadeia de caracteres que foi passada no parâmetro **FriendlyName** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span><span class="sxs-lookup"><span data-stu-id="5a44d-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-124">A mesma cadeia de caracteres que foi passada no parâmetro **ListType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="5a44d-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="5a44d-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="5a44d-126">A mesma cadeia de caracteres que foi passada no parâmetro **ViewMode** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="5a44d-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a44d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a44d-127">Requirements</span></span>



| <span data-ttu-id="5a44d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a44d-128">Requirement</span></span> | <span data-ttu-id="5a44d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5a44d-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a44d-130">Versão</span><span class="sxs-lookup"><span data-stu-id="5a44d-130">Version</span></span><br/> | <span data-ttu-id="5a44d-131">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5a44d-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="5a44d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a44d-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a44d-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a44d-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a44d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a44d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a44d-135">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5a44d-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





