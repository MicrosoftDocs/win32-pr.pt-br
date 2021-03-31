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
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>\_Atributo de \_ \_ ID do \_ \_ formato de metadados de objeto de áudio \_ espacial \_ do MF MT

Um GUID definido pelo decodificador que identifica o formato de metadados de áudio espacial, notificando os componentes downstream do tipo de objeto de metadados que o decodificador produzirá.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . O blob de metadados é opaco para o pipeline de Media Foundation e os componentes. O atributo é aplicado ao tipo de mídia de áudio espacial. Se um componente downstream não oferecer suporte ao formato de metadados especificado pelo GUID, o componente deverá rejeitar o tipo de mídia de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
