---
description: Desabilita o uso de plug-ins de câmera de pós-processamento pelo leitor de origem.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Atributo MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171604"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="7fabd-103">\_Leitor de origem MF \_ \_ desabilitar atributo de plug- \_ ins de câmera \_</span><span class="sxs-lookup"><span data-stu-id="7fabd-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="7fabd-104">Desabilita o uso de plug-ins de câmera de pós-processamento pelo [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="7fabd-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="7fabd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7fabd-105">Data type</span></span>

<span data-ttu-id="7fabd-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7fabd-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7fabd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fabd-107">Remarks</span></span>

<span data-ttu-id="7fabd-108">Esse atributo se aplica quando o leitor de origem é usado com uma fonte de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7fabd-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="7fabd-109">Se esse atributo for **true**, ele impedirá que o leitor de origem carregue quaisquer plug-ins de pós-processamento que possam ser fornecidos pela câmera.</span><span class="sxs-lookup"><span data-stu-id="7fabd-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="7fabd-110">Caso contrário, por padrão, o leitor de origem os carregará.</span><span class="sxs-lookup"><span data-stu-id="7fabd-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="7fabd-111">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="7fabd-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="7fabd-112">Defina o atributo ao criar o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="7fabd-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fabd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fabd-113">Requirements</span></span>



| <span data-ttu-id="7fabd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fabd-114">Requirement</span></span> | <span data-ttu-id="7fabd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7fabd-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fabd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fabd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7fabd-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fabd-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7fabd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fabd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7fabd-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fabd-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7fabd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fabd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fabd-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fabd-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fabd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fabd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fabd-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7fabd-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fabd-124">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="7fabd-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




