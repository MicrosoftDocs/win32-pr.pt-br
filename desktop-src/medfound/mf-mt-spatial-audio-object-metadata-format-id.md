---
description: Um GUID definido pelo decodificador que identifica o formato de metadados de áudio espacial, notificando os componentes downstream do tipo de objeto de metadados que o decodificador será produzido.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b43751655f2a583d50c8de3fe108babcaa08d11d78df552b6ddf1f10e413be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955496"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>Atributo \_ MF MT \_ SPATIAL \_ AUDIO OBJECT \_ \_ METADATA FORMAT \_ \_ ID

Um GUID definido pelo decodificador que identifica o formato de metadados de áudio espacial, notificando os componentes downstream do tipo de objeto de metadados que o decodificador será produzido.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader.**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) O blob de metadados é opaco para o pipeline Media Foundation e os componentes. O atributo é aplicado ao tipo de mídia de áudio espacial. Se um componente downstream não dá suporte ao formato de metadados especificado pelo GUID, o componente deve rejeitar o tipo de mídia de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
