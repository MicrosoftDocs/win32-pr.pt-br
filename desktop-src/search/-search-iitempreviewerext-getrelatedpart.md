---
description: Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Método IItemPreviewerExt:: GetRelatedPart'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785183"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="87ef0-103">Método IItemPreviewerExt:: GetRelatedPart</span><span class="sxs-lookup"><span data-stu-id="87ef0-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="87ef0-104">Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.</span><span class="sxs-lookup"><span data-stu-id="87ef0-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ef0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87ef0-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="87ef0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87ef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ef0-107">*dwContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ef0-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="87ef0-108">Type: **DWORD**</span></span>

<span data-ttu-id="87ef0-109">O identificador de contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="87ef0-109">The context identifier for the operation.</span></span> <span data-ttu-id="87ef0-110">Substitua o padrão **dwContext** para definir o identificador de contexto como um valor de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="87ef0-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="87ef0-111">*pwszProp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ef0-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="87ef0-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="87ef0-113">Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="87ef0-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="87ef0-114">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ef0-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="87ef0-115">Type: **DWORD**</span></span>

<span data-ttu-id="87ef0-116">Um valor inteiro longo sem sinal que contém o índice de base zero da parte do corpo relacionado.</span><span class="sxs-lookup"><span data-stu-id="87ef0-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="87ef0-117">*pInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="87ef0-118">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="87ef0-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="87ef0-119">Recebe um ponteiro para a estrutura [_ *LINKINFO* \*](-search-linkinfo.md) na qual o método retorna informações sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="87ef0-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="87ef0-120">*pInfo* não deve ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="87ef0-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ef0-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87ef0-121">Return value</span></span>

<span data-ttu-id="87ef0-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="87ef0-122">Type: **HRESULT**</span></span>

<span data-ttu-id="87ef0-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="87ef0-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87ef0-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87ef0-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ef0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="87ef0-125">Remarks</span></span>

<span data-ttu-id="87ef0-126">A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="87ef0-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="87ef0-127">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="87ef0-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ef0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ef0-128">Requirements</span></span>



| <span data-ttu-id="87ef0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ef0-129">Requirement</span></span> | <span data-ttu-id="87ef0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="87ef0-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87ef0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ef0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="87ef0-132">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87ef0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ef0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="87ef0-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87ef0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87ef0-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="87ef0-135">Redistributable</span></span><br/>          | <span data-ttu-id="87ef0-136">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="87ef0-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="87ef0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="87ef0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ef0-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="87ef0-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




