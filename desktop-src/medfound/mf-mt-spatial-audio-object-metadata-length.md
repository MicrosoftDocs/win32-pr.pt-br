---
description: Um valor que especifica o tamanho, em bytes, do tipo de objeto de metadados de áudio espacial que o decodificador será produzido.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784e1b210b616f4c42c2c3d410a207adc9c8c8ccaf751432cb027a7cc30cf951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876807"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>Atributo MF \_ MT \_ SPATIAL AUDIO OBJECT \_ \_ \_ METADATA \_ LENGTH

Um valor que especifica o tamanho, em bytes, do tipo de objeto de metadados de áudio espacial que o decodificador será produzido.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O blob de metadados com o formato especificado é escrito usando a interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e lido usando a interface [**ISpatialAudioMetadataReader.**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) O blob de metadados é opaco para o pipeline Media Foundation e componentes. O atributo é aplicado ao tipo de mídia de áudio espacial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
