---
description: Especifica se uma Media Foundation de transformação (MFT) executa o processamento assíncrono.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Atributo MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647562"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="786cf-103">\_Atributo assíncrono de transformação MF \_</span><span class="sxs-lookup"><span data-stu-id="786cf-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="786cf-104">Especifica se uma Media Foundation de transformação (MFT) executa o processamento assíncrono.</span><span class="sxs-lookup"><span data-stu-id="786cf-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="786cf-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="786cf-105">Data type</span></span>

<span data-ttu-id="786cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="786cf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="786cf-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="786cf-107">Get/set</span></span>

<span data-ttu-id="786cf-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="786cf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="786cf-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="786cf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="786cf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="786cf-110">Remarks</span></span>

<span data-ttu-id="786cf-111">O atributo é um valor booliano:</span><span class="sxs-lookup"><span data-stu-id="786cf-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="786cf-112">Se o atributo for diferente de zero, o MFT executará o processamento assíncrono.</span><span class="sxs-lookup"><span data-stu-id="786cf-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="786cf-113">Se o atributo for 0 ou não definido, o MFT será síncrono.</span><span class="sxs-lookup"><span data-stu-id="786cf-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="786cf-114">Para obter esse atributo, primeiro chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributos da MFT.</span><span class="sxs-lookup"><span data-stu-id="786cf-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="786cf-115">Se esse método tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="786cf-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="786cf-116">Se um dos dois métodos falhar, o MFT será síncrono.</span><span class="sxs-lookup"><span data-stu-id="786cf-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="786cf-117">Para MFTs assíncronas, esse atributo deve ser definido como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="786cf-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="786cf-118">Para MFTs síncronos, esse atributo é opcional, mas deve ser definido como 0, se estiver presente.</span><span class="sxs-lookup"><span data-stu-id="786cf-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="786cf-119">MFTs assíncronas não são compatíveis com versões anteriores do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="786cf-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="786cf-120">Para usar uma MFT assíncrona, o cliente deve definir o atributo de [**\_ \_ \_ desbloqueio do MF Transform Async**](mf-transform-async-unlock.md) no MFT.</span><span class="sxs-lookup"><span data-stu-id="786cf-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="786cf-121">(O pipeline de Microsoft Media Foundation executa essa etapa automaticamente.)</span><span class="sxs-lookup"><span data-stu-id="786cf-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="786cf-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="786cf-122">Examples</span></span>

<span data-ttu-id="786cf-123">O código a seguir testa se uma MFT executa o processamento assíncrono.</span><span class="sxs-lookup"><span data-stu-id="786cf-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="786cf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="786cf-124">Requirements</span></span>



| <span data-ttu-id="786cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="786cf-125">Requirement</span></span> | <span data-ttu-id="786cf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="786cf-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="786cf-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="786cf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="786cf-128">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="786cf-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="786cf-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="786cf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="786cf-130">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="786cf-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="786cf-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="786cf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="786cf-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="786cf-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786cf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="786cf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786cf-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="786cf-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="786cf-135">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="786cf-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="786cf-136">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="786cf-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="786cf-137">**\_desbloqueio assíncrono de transformação MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="786cf-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




