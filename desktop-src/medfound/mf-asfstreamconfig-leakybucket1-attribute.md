---
description: Define a média &\# 0034; o Bucket de vazamento&\# 0034; parâmetros (consulte comentários) para codificar um arquivo de mídia do Windows. Defina esse atributo usando a interface IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Atributo MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759860"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="69f66-104">\_Atributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET1</span><span class="sxs-lookup"><span data-stu-id="69f66-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="69f66-105">Define os parâmetros médios de "Bucket de vazamentos" (consulte comentários) para codificar um arquivo de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="69f66-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="69f66-106">Defina esse atributo usando a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="69f66-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="69f66-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="69f66-107">Data type</span></span>

<span data-ttu-id="69f66-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="69f66-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="69f66-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="69f66-109">Remarks</span></span>

<span data-ttu-id="69f66-110">O valor desse atributo é uma matriz de três **DWORD** s, na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="69f66-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="69f66-111">Taxa de bits, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="69f66-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="69f66-112">Janela buffer, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="69f66-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="69f66-113">Total do buffer inicial, em bytes.</span><span class="sxs-lookup"><span data-stu-id="69f66-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="69f66-114">Para obter mais informações sobre o conceito de Bucket de vazamento, consulte o tópico [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md) na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="69f66-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="69f66-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69f66-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f66-116">Requirements</span></span>



| <span data-ttu-id="69f66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f66-117">Requirement</span></span> | <span data-ttu-id="69f66-118">Valor</span><span class="sxs-lookup"><span data-stu-id="69f66-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f66-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69f66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69f66-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69f66-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69f66-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69f66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69f66-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69f66-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="69f66-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69f66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69f66-124"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f66-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f66-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="69f66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f66-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69f66-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69f66-127">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="69f66-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="69f66-128">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="69f66-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="69f66-129">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="69f66-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="69f66-130">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="69f66-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




