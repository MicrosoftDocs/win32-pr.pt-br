---
description: Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Método ISearchProtocolUI:: GetSearchItemForUrl'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646874"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="dd521-104">Método ISearchProtocolUI:: GetSearchItemForUrl</span><span class="sxs-lookup"><span data-stu-id="dd521-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="dd521-105">Obtém o item de pesquisa para os dados especificados.</span><span class="sxs-lookup"><span data-stu-id="dd521-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="dd521-106">Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dd521-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd521-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd521-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="dd521-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd521-109">*pcwszURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd521-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd521-110">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="dd521-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="dd521-111">Ponteiro para uma cadeia de caracteres Unicode terminada em dados nulos contendo o item de pesquisa para a URL que está sendo acessada.</span><span class="sxs-lookup"><span data-stu-id="dd521-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="dd521-112">*pPropertyBag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd521-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd521-113">Tipo: \**IItemPropertyBag \** _</span><span class="sxs-lookup"><span data-stu-id="dd521-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="dd521-114">Ponteiro para um objeto [_ *IItemPropertyBag* \*](iitempropertybag.md) que contém informações sobre o item de pesquisa, incluindo as propriedades do item.</span><span class="sxs-lookup"><span data-stu-id="dd521-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="dd521-115">*ppSearchItem* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dd521-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dd521-116">Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dd521-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="dd521-117">Recebe o endereço de um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) criado por esse método.</span><span class="sxs-lookup"><span data-stu-id="dd521-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="dd521-118">Esse objeto contém informações sobre o item de pesquisa, como o nome do arquivo do item.</span><span class="sxs-lookup"><span data-stu-id="dd521-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd521-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd521-119">Return value</span></span>

<span data-ttu-id="dd521-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd521-120">Type: **HRESULT**</span></span>

<span data-ttu-id="dd521-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd521-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd521-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd521-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd521-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd521-123">Remarks</span></span>

<span data-ttu-id="dd521-124">O método **ISearchProtocolUI:: GetSearchItemForUrl** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="dd521-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="dd521-125">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchProtocolUI**](-search-isearchprotocolui.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="dd521-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd521-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd521-126">Requirements</span></span>



| <span data-ttu-id="dd521-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd521-127">Requirement</span></span> | <span data-ttu-id="dd521-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dd521-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd521-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd521-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd521-130">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="dd521-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd521-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd521-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd521-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd521-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd521-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="dd521-133">Redistributable</span></span><br/>          | <span data-ttu-id="dd521-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="dd521-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dd521-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd521-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd521-136">**ISearchProtocolUI**</span><span class="sxs-lookup"><span data-stu-id="dd521-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




