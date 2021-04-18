---
description: Define a prioridade base para threads de processamento de áudio criados pelo leitor de origem ou gravador de coletor.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Atributo MF_READWRITE_MMCSS_PRIORITY_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789371"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a><span data-ttu-id="dcbb2-103">Atributo de áudio do MF \_ ReadWrite \_ MMCSS \_ Priority \_</span><span class="sxs-lookup"><span data-stu-id="dcbb2-103">MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO attribute</span></span>

<span data-ttu-id="dcbb2-104">Define a prioridade base para threads de processamento de áudio criados pelo leitor de origem ou gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="dcbb2-104">Sets the base priority for audio-processing threads created by the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcbb2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dcbb2-105">Data type</span></span>

<span data-ttu-id="dcbb2-106">**INT32** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="dcbb2-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="dcbb2-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="dcbb2-107">Get/set</span></span>

<span data-ttu-id="dcbb2-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="dcbb2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="dcbb2-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="dcbb2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="dcbb2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcbb2-110">Remarks</span></span>

<span data-ttu-id="dcbb2-111">Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="dcbb2-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="dcbb2-112">Se você definir esse atributo, defina também o atributo de [ \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="dcbb2-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute.</span></span> <span data-ttu-id="dcbb2-113">Caso contrário, esse atributo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="dcbb2-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="dcbb2-114">Quando o leitor de origem ou o gravador de coletor registra threads de processamento de áudio com o [serviço de Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md), o valor desse atributo especifica a prioridade de thread base.</span><span class="sxs-lookup"><span data-stu-id="dcbb2-114">When the Source Reader or Sink Writer registers audio-processing threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="dcbb2-115">Se esse atributo não for definido, o valor padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="dcbb2-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbb2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcbb2-116">Requirements</span></span>



| <span data-ttu-id="dcbb2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcbb2-117">Requirement</span></span> | <span data-ttu-id="dcbb2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dcbb2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbb2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcbb2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcbb2-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dcbb2-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="dcbb2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcbb2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcbb2-122">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dcbb2-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dcbb2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcbb2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcbb2-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbb2-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbb2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcbb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbb2-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dcbb2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
