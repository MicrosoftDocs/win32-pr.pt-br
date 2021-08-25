---
description: Conclui todas as operações necessárias no buffer de metadados e libera o objeto ISpatialAudioMetadataItems especificado.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Método ISpatialAudioMetadataWriter:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 4b29efb38cf11ba718a631f676323eb3db93aab042c70691dfb89ce957266e86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875416"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>Método ISpatialAudioMetadataWriter:: Close

Conclui todas as operações necessárias no buffer de metadados e libera o objeto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, os códigos de retorno possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                                                                     | Descrição                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nenhum \_ item \_ aberto**</dt> </dl>            | O [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) fornecido não foi aberto com uma chamada para [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nenhum \_ item \_ gravado**</dt> </dl>         | Nenhum item de metadados foi gravado no [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornecido.<br/>                                              |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ item \_ deve \_ ter \_ comandos**</dt> </dl> | Nenhum comando de metadados foi gravado no [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornecido.<br/>                                           |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




