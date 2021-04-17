---
description: Especifica uma classe de serviço do Agendador de classes de multimídia (MMCSS) para threads de processamento de áudio no leitor de origem ou no gravador de coletor.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Atributo MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812185"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="98dbc-103">\_Atributo de \_ \_ áudio da classe MF ReadWrite MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="98dbc-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="98dbc-104">Especifica uma classe de [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para threads de processamento de áudio no leitor de origem ou no gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="98dbc-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="98dbc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="98dbc-105">Data type</span></span>

<span data-ttu-id="98dbc-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="98dbc-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="98dbc-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="98dbc-107">Get/set</span></span>

<span data-ttu-id="98dbc-108">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="98dbc-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="98dbc-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="98dbc-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="98dbc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="98dbc-110">Remarks</span></span>

<span data-ttu-id="98dbc-111">Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="98dbc-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="98dbc-112">O valor do atributo deve ser um nome de classe do MMCSS válido.</span><span class="sxs-lookup"><span data-stu-id="98dbc-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="98dbc-113">Se esse atributo for definido, o leitor de origem ou o gravador de coletor registrará seus threads de processamento de áudio com a classe do MMCSS especificada.</span><span class="sxs-lookup"><span data-stu-id="98dbc-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="98dbc-114">O MMCSS garante que o processamento de dados no leitor de origem ou no gravador de coletor tenha prioridade sobre outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="98dbc-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="98dbc-115">Para especificar a prioridade base para threads de áudio, defina o atributo de [áudio do MF \_ ReadWrite \_ MMCSS \_ Priority \_ ](mf-readwrite-mmcss-priority-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="98dbc-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="98dbc-116">Se esse atributo não estiver definido, a prioridade base para threads de áudio será zero.</span><span class="sxs-lookup"><span data-stu-id="98dbc-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="98dbc-117">Esse atributo substitui o atributo de [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) para threads de processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="98dbc-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="98dbc-118">Se nenhum atributo for definido, os threads de áudio não serão registrados com MCSS.</span><span class="sxs-lookup"><span data-stu-id="98dbc-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="98dbc-119">Para a maioria dos aplicativos, a falha de áudio é muito mais perceptível para o usuário do que a falha de vídeo e, portanto, menos aceitável.</span><span class="sxs-lookup"><span data-stu-id="98dbc-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="98dbc-120">Por esse motivo, um aplicativo normalmente deve definir o \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ para uma classe do MMCSS de prioridade mais alta do que a [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md).</span><span class="sxs-lookup"><span data-stu-id="98dbc-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="98dbc-121">Isso garante que o processamento de áudio receba prioridade mais alta do que outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="98dbc-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="98dbc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98dbc-122">Requirements</span></span>



| <span data-ttu-id="98dbc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98dbc-123">Requirement</span></span> | <span data-ttu-id="98dbc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="98dbc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98dbc-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98dbc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="98dbc-126">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="98dbc-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="98dbc-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98dbc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="98dbc-128">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="98dbc-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="98dbc-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98dbc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="98dbc-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="98dbc-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98dbc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="98dbc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98dbc-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98dbc-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
