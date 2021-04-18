---
description: Indica se um fluxo contém conteúdo protegido.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Atributo MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793896"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="24a44-103">\_ \_ Atributo protegido do MF SD</span><span class="sxs-lookup"><span data-stu-id="24a44-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="24a44-104">Indica se um fluxo contém conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="24a44-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="24a44-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="24a44-105">Data type</span></span>

<span data-ttu-id="24a44-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="24a44-106">**UINT32**</span></span>

<span data-ttu-id="24a44-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="24a44-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a44-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="24a44-108">Remarks</span></span>

<span data-ttu-id="24a44-109">Esse atributo se aplica a descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="24a44-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="24a44-110">Se o valor do atributo for **true**, o fluxo conterá conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="24a44-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="24a44-111">Se o valor for **false** ou o atributo não estiver definido, o fluxo conterá limpar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="24a44-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="24a44-112">Em vez de verificar cada fluxo para esse atributo, você pode passar um descritor de apresentação para a função [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) .</span><span class="sxs-lookup"><span data-stu-id="24a44-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="24a44-113">Essa função testa se o descritor de apresentação contém quaisquer fluxos protegidos.</span><span class="sxs-lookup"><span data-stu-id="24a44-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="24a44-114">Uma fonte de mídia deve definir esse atributo no descritor de fluxo se o conteúdo exigir o caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="24a44-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="24a44-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="24a44-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="24a44-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24a44-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="24a44-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a44-117">Requirements</span></span>



| <span data-ttu-id="24a44-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a44-118">Requirement</span></span> | <span data-ttu-id="24a44-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24a44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24a44-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24a44-121">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="24a44-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="24a44-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24a44-123">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="24a44-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="24a44-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24a44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a44-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a44-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a44-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="24a44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a44-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24a44-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="24a44-128">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="24a44-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="24a44-129">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="24a44-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="24a44-130">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="24a44-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="24a44-131">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="24a44-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




