---
description: Um valor que especifica o tamanho, em bytes, do tipo de objeto de metadados de áudio espacial que o decodificador produzirá.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: Atributo MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169759"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="24b34-103">\_Atributo de \_ \_ comprimento dos \_ metadados do objeto de áudio espacial \_ do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="24b34-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="24b34-104">Um valor que especifica o tamanho, em bytes, do tipo de objeto de metadados de áudio espacial que o decodificador produzirá.</span><span class="sxs-lookup"><span data-stu-id="24b34-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="24b34-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="24b34-105">Data type</span></span>

<span data-ttu-id="24b34-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="24b34-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="24b34-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="24b34-107">Remarks</span></span>

<span data-ttu-id="24b34-108">O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="24b34-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="24b34-109">O blob de metadados é opaco para o pipeline de Media Foundation e os componentes.</span><span class="sxs-lookup"><span data-stu-id="24b34-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="24b34-110">O atributo é aplicado ao tipo de mídia de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="24b34-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b34-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b34-111">Requirements</span></span>



| <span data-ttu-id="24b34-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b34-112">Requirement</span></span> | <span data-ttu-id="24b34-113">Valor</span><span class="sxs-lookup"><span data-stu-id="24b34-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24b34-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b34-114">Minimum supported client</span></span><br/> | <span data-ttu-id="24b34-115">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="24b34-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="24b34-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b34-116">Minimum supported server</span></span><br/> | <span data-ttu-id="24b34-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="24b34-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="24b34-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b34-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b34-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b34-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
