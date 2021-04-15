---
description: Habilita o uso de uma Media Foundation de transformação assíncrona (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Atributo MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502105"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="6a0c8-103">\_Atributo de \_ desbloqueio assíncrono de transformação MF \_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="6a0c8-104">Habilita o uso de uma Media Foundation de transformação assíncrona (MFT).</span><span class="sxs-lookup"><span data-stu-id="6a0c8-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="6a0c8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6a0c8-105">Data type</span></span>

<span data-ttu-id="6a0c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6a0c8-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="6a0c8-107">Get/set</span></span>

<span data-ttu-id="6a0c8-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6a0c8-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6a0c8-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6a0c8-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a0c8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a0c8-110">Remarks</span></span>

<span data-ttu-id="6a0c8-111">MFTs assíncronas não são compatíveis com versões anteriores do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="6a0c8-112">Para evitar que aplicativos existentes acidentalmente usem uma MFT assíncrona, esse atributo deve ser definido como um valor diferente de zero antes que uma MFT assíncrona possa ser usada.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="6a0c8-113">O pipeline de Media Foundation define automaticamente o atributo, para que a maioria dos aplicativos não precise usar esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="6a0c8-114">No entanto, se um aplicativo usar uma MFT assíncrona fora do pipeline de Media Foundation, o aplicativo deverá definir esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="6a0c8-115">Os MFTs síncronos não exigem esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="6a0c8-116">Para testar se uma MFT é assíncrona, obtenha o valor do [atributo \_ \_ assíncrono de transformação MF](mf-transform-async.md) na MFT.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="6a0c8-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a0c8-117">Examples</span></span>

<span data-ttu-id="6a0c8-118">O código a seguir desbloqueia uma MFT assíncrona.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6a0c8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a0c8-119">Requirements</span></span>



| <span data-ttu-id="6a0c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a0c8-120">Requirement</span></span> | <span data-ttu-id="6a0c8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6a0c8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a0c8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a0c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a0c8-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6a0c8-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6a0c8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a0c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a0c8-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6a0c8-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6a0c8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a0c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a0c8-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a0c8-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a0c8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a0c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a0c8-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a0c8-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a0c8-130">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="6a0c8-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="6a0c8-131">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="6a0c8-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




