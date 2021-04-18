---
description: Define o pico &\# 0034; Bucket de vazamento&\# 0034; parâmetros (consulte comentários) para codificar um arquivo de mídia do Windows. Esses parâmetros são usados para a taxa de bits de pico. Defina esse atributo usando a interface IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Atributo MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785326"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="7b0c2-105">\_Atributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET2</span><span class="sxs-lookup"><span data-stu-id="7b0c2-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="7b0c2-106">Define o pico dos parâmetros de "Bucket de vazamentos" (consulte comentários) para codificar um arquivo de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="7b0c2-107">Esses parâmetros são usados para a taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="7b0c2-108">Defina esse atributo usando a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="7b0c2-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b0c2-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7b0c2-109">Data type</span></span>

<span data-ttu-id="7b0c2-110">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="7b0c2-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7b0c2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b0c2-111">Remarks</span></span>

<span data-ttu-id="7b0c2-112">O valor desse atributo é uma matriz de três **DWORD** s, na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="7b0c2-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="7b0c2-113">Taxa de bits, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="7b0c2-114">Janela buffer, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="7b0c2-115">Total do buffer inicial, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="7b0c2-116">Para obter mais informações sobre o conceito de Bucket de vazamento, consulte o tópico [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md) na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="7b0c2-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7b0c2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0c2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b0c2-118">Requirements</span></span>



| <span data-ttu-id="7b0c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0c2-119">Requirement</span></span> | <span data-ttu-id="7b0c2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b0c2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0c2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0c2-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b0c2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7b0c2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0c2-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b0c2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7b0c2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b0c2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b0c2-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b0c2-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0c2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b0c2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0c2-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b0c2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b0c2-129">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="7b0c2-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b0c2-130">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="7b0c2-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7b0c2-131">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="7b0c2-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7b0c2-132">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="7b0c2-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




