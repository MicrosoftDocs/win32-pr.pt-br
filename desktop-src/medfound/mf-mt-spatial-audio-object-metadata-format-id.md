---
description: Um GUID definido pelo decodificador que identifica o formato de metadados de áudio espacial, notificando os componentes downstream do tipo de objeto de metadados que o decodificador produzirá.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: Atributo MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169760"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="8803f-103">\_Atributo de \_ \_ ID do \_ \_ formato de metadados de objeto de áudio \_ espacial \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="8803f-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="8803f-104">Um GUID definido pelo decodificador que identifica o formato de metadados de áudio espacial, notificando os componentes downstream do tipo de objeto de metadados que o decodificador produzirá.</span><span class="sxs-lookup"><span data-stu-id="8803f-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="8803f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8803f-105">Data type</span></span>

<span data-ttu-id="8803f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8803f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8803f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8803f-107">Remarks</span></span>

<span data-ttu-id="8803f-108">O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="8803f-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="8803f-109">O blob de metadados é opaco para o pipeline de Media Foundation e os componentes.</span><span class="sxs-lookup"><span data-stu-id="8803f-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="8803f-110">O atributo é aplicado ao tipo de mídia de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8803f-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="8803f-111">Se um componente downstream não oferecer suporte ao formato de metadados especificado pelo GUID, o componente deverá rejeitar o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="8803f-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8803f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8803f-112">Requirements</span></span>



| <span data-ttu-id="8803f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8803f-113">Requirement</span></span> | <span data-ttu-id="8803f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8803f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8803f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8803f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8803f-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="8803f-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8803f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8803f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8803f-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8803f-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8803f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8803f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8803f-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8803f-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
