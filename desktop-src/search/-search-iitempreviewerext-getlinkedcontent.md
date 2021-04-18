---
description: Permite a extensão para o conteúdo avançado de uma propriedade.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Método IItemPreviewerExt:: GetLinkedContent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764286"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="c672a-103">Método IItemPreviewerExt:: GetLinkedContent</span><span class="sxs-lookup"><span data-stu-id="c672a-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="c672a-104">Permite a extensão para o conteúdo avançado de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c672a-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c672a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c672a-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c672a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c672a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c672a-107">*dwContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c672a-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c672a-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c672a-108">Type: **DWORD**</span></span>

<span data-ttu-id="c672a-109">O identificador de contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="c672a-109">The context identifier for the operation.</span></span> <span data-ttu-id="c672a-110">Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="c672a-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="c672a-111">*pwszProp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c672a-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c672a-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="c672a-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="c672a-113">Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c672a-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="c672a-114">*pInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c672a-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c672a-115">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c672a-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="c672a-116">Recebe um ponteiro para a estrutura [_ *LINKINFO* \*](-search-linkinfo.md) na qual o método retorna informações sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="c672a-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="c672a-117">*pInfo* não deve ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c672a-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c672a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c672a-118">Return value</span></span>

<span data-ttu-id="c672a-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c672a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="c672a-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c672a-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c672a-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c672a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c672a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c672a-122">Remarks</span></span>

<span data-ttu-id="c672a-123">A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="c672a-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="c672a-124">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="c672a-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c672a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c672a-125">Requirements</span></span>



| <span data-ttu-id="c672a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c672a-126">Requirement</span></span> | <span data-ttu-id="c672a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c672a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c672a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c672a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c672a-129">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="c672a-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c672a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c672a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c672a-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c672a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c672a-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c672a-132">Redistributable</span></span><br/>          | <span data-ttu-id="c672a-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="c672a-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c672a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c672a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c672a-135">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="c672a-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




