---
description: Especifica uma classe de serviço do Agendador de classes de multimídia (MMCSS) para o leitor de origem ou o gravador de coletor.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Atributo MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663014"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="b3dec-103">\_Atributo de classe MF ReadWrite \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="b3dec-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="b3dec-104">Especifica uma classe de [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para o leitor de origem ou o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="b3dec-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3dec-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b3dec-105">Data type</span></span>

<span data-ttu-id="b3dec-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b3dec-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="b3dec-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b3dec-107">Get/set</span></span>

<span data-ttu-id="b3dec-108">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b3dec-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b3dec-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b3dec-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3dec-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3dec-110">Remarks</span></span>

<span data-ttu-id="b3dec-111">Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="b3dec-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="b3dec-112">O valor do atributo deve ser um nome de classe do MMCSS válido.</span><span class="sxs-lookup"><span data-stu-id="b3dec-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="b3dec-113">Se esse atributo for definido, o leitor de origem ou o gravador do coletor registrará todos os seus threads com a classe do MMCSS especificada.</span><span class="sxs-lookup"><span data-stu-id="b3dec-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="b3dec-114">O MMCSS garante que o processamento de dados no leitor de origem ou no gravador de coletor tenha prioridade sobre outras tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="b3dec-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="b3dec-115">Para especificar a prioridade base, defina o atributo de [ \_ \_ \_ prioridade MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) .</span><span class="sxs-lookup"><span data-stu-id="b3dec-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="b3dec-116">Se esse atributo não estiver definido, a prioridade base será zero.</span><span class="sxs-lookup"><span data-stu-id="b3dec-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="b3dec-117">Para threads de processamento de áudio, o atributo de [ \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) (se definido) substitui esse atributo.</span><span class="sxs-lookup"><span data-stu-id="b3dec-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3dec-118">Requirements</span></span>



| <span data-ttu-id="b3dec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3dec-119">Requirement</span></span> | <span data-ttu-id="b3dec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b3dec-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dec-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3dec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3dec-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3dec-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b3dec-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3dec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3dec-124">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3dec-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b3dec-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3dec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3dec-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3dec-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3dec-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3dec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dec-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3dec-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
