---
description: Especifica o número máximo de objetos de áudio dinâmicos que podem ser processados pelo ponto de extremidade de áudio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Atributo MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749516"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>\_Atributo de \_ máximo \_ de \_ \_ objetos dinâmicos de áudio \_ do MF MT

Especifica o número máximo de objetos de áudio dinâmicos que podem ser processados pelo ponto de extremidade de áudio simulataneously.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Um [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) pode conter menos amostras do que o número especificado por esse atributo. Se um exemplo contiver mais objetos de áudio do que o especificado por esse atributo, o comportamento será indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




