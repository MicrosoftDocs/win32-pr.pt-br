---
description: Especifica uma classe MMCSS (Serviço de Agendador de Classe Multimídia) para threads de processamento de áudio no Leitor de Origem ou no Sink Writer.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f416c22619c0777ef244e6566328154bf7a7336587fc73a3f29626fcdaa1c462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345276"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>Atributo DE ÁUDIO \_ \_ DA CLASSE MMCSS MF READWRITE \_ \_

Especifica uma classe [MMCSS (Serviço](../procthread/multimedia-class-scheduler-service.md) de Agendador de Classe Multimídia) para threads de processamento de áudio no Leitor de Origem ou no Sink Writer.

## <a name="data-type"></a>Tipo de dados

**Lpwstr**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Opcionalmente, de definir esse atributo ao criar uma instância do Leitor de [Origem](source-reader.md) ou [do Sink Writer.](sink-writer.md) O valor do atributo deve ser um nome de classe MMCSS válido.

Se esse atributo for definido, o Leitor de Origem ou o Sink Writer registrará seus threads de processamento de áudio com a classe MMCSS especificada. O MMCSS garante que o processamento de dados no Leitor de Origem ou no Sink Writer tenha prioridade sobre outras tarefas do sistema.

Para especificar a prioridade base para threads de áudio, de definir o atributo [MF \_ READWRITE \_ MMCSS \_ PRIORITY \_ AUDIO.](mf-readwrite-mmcss-priority-audio.md) Se esse atributo não estiver definido, a prioridade base para threads de áudio será zero.

Esse atributo substitui o atributo [MF \_ READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md) para threads de processamento de áudio. Se nenhum atributo estiver definido, os threads de áudio não serão registrados com o MCSS.

Para a maioria dos aplicativos, a falha de áudio é muito mais perceptível para o usuário do que a falha de vídeo e, portanto, menos aceitável. Por esse motivo, um aplicativo normalmente deve definir MF READWRITE MMCSS CLASS AUDIO como uma classe MMCSS de prioridade mais alta do que \_ \_ a CLASSE \_ \_ [ \_ MMCSS READWRITE \_ \_ MF](mf-readwrite-mmcss-class.md). Isso garante que o processamento de áudio recebe prioridade mais alta do que outras tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
