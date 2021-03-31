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
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>\_Atributo de \_ \_ comprimento dos \_ metadados do objeto de áudio espacial \_ do MF MT \_

Um valor que especifica o tamanho, em bytes, do tipo de objeto de metadados de áudio espacial que o decodificador produzirá.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . O blob de metadados é opaco para o pipeline de Media Foundation e os componentes. O atributo é aplicado ao tipo de mídia de áudio espacial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
