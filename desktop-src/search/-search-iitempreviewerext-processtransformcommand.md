---
description: Permite o processamento de um comando de transformação encontrado em um modelo de visualização.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: 'IItemPreviewerExt: método rocessTransformCommand de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826916"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="61cea-103">IItemPreviewerExt: método rocessTransformCommand de:P</span><span class="sxs-lookup"><span data-stu-id="61cea-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="61cea-104">Permite o processamento de um comando de transformação encontrado em um modelo de visualização.</span><span class="sxs-lookup"><span data-stu-id="61cea-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61cea-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="61cea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61cea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cea-107">*dwContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61cea-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cea-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="61cea-108">Type: **DWORD**</span></span>

<span data-ttu-id="61cea-109">O identificador de contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="61cea-109">The context identifier for the operation.</span></span> <span data-ttu-id="61cea-110">Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="61cea-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="61cea-111">*pwszName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61cea-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cea-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="61cea-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="61cea-113">Um ponteiro para o nome do comando de transformação como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="61cea-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="61cea-114">*pwszArg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61cea-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cea-115">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="61cea-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="61cea-116">Um ponteiro para o argumento como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="61cea-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="61cea-117">*pVarResult* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="61cea-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="61cea-118">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="61cea-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="61cea-119">Um ponteiro para a variante de resultado.</span><span class="sxs-lookup"><span data-stu-id="61cea-119">A pointer to the result variant.</span></span> <span data-ttu-id="61cea-120">_pvarResult \* não deve ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="61cea-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cea-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61cea-121">Return value</span></span>

<span data-ttu-id="61cea-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="61cea-122">Type: **HRESULT**</span></span>

<span data-ttu-id="61cea-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="61cea-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61cea-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61cea-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61cea-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="61cea-125">Remarks</span></span>

<span data-ttu-id="61cea-126">A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="61cea-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="61cea-127">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="61cea-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cea-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cea-128">Requirements</span></span>



| <span data-ttu-id="61cea-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cea-129">Requirement</span></span> | <span data-ttu-id="61cea-130">Valor</span><span class="sxs-lookup"><span data-stu-id="61cea-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61cea-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cea-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61cea-132">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="61cea-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61cea-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cea-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61cea-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61cea-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61cea-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="61cea-135">Redistributable</span></span><br/>          | <span data-ttu-id="61cea-136">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="61cea-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="61cea-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="61cea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cea-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="61cea-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




