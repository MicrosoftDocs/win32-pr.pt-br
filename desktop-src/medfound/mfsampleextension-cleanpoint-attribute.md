---
description: Indica se um exemplo é um ponto de acesso aleatório.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: Atributo MFSampleExtension_CleanPoint (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502287"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="3c241-103">\_Atributo MFSampleExtension CleanPoint</span><span class="sxs-lookup"><span data-stu-id="3c241-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="3c241-104">Indica se um exemplo é um ponto de acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="3c241-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c241-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3c241-105">Data type</span></span>

<span data-ttu-id="3c241-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c241-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3c241-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="3c241-107">Get/set</span></span>

<span data-ttu-id="3c241-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3c241-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3c241-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3c241-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3c241-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="3c241-110">Applies to</span></span>

[<span data-ttu-id="3c241-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="3c241-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="3c241-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c241-112">Remarks</span></span>

<span data-ttu-id="3c241-113">Esse atributo se aplica a exemplos.</span><span class="sxs-lookup"><span data-stu-id="3c241-113">This attribute applies to samples.</span></span> <span data-ttu-id="3c241-114">Se o atributo for **true**, o exemplo será um ponto de acesso aleatório e a decodificação poderá começar com esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="3c241-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="3c241-115">Caso contrário, o exemplo não é um ponto de acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="3c241-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="3c241-116">Se esse atributo não for definido, o valor padrão será **false**.</span><span class="sxs-lookup"><span data-stu-id="3c241-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="3c241-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3c241-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="3c241-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c241-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="3c241-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c241-119">Requirements</span></span>



| <span data-ttu-id="3c241-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c241-120">Requirement</span></span> | <span data-ttu-id="3c241-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3c241-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c241-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c241-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c241-123">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c241-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3c241-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c241-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c241-125">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c241-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3c241-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c241-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c241-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c241-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c241-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c241-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c241-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c241-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c241-130">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="3c241-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c241-131">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="3c241-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




