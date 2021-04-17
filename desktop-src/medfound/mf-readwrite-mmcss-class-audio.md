---
description: Especifica uma classe de serviço do Agendador de classes de multimídia (MMCSS) para threads de processamento de áudio no leitor de origem ou no gravador de coletor.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Atributo MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812185"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>\_Atributo de \_ \_ áudio da classe MF ReadWrite MMCSS \_

Especifica uma classe de [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para threads de processamento de áudio no leitor de origem ou no gravador de coletor.

## <a name="data-type"></a>Tipo de dados

**LPWSTR**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md). O valor do atributo deve ser um nome de classe do MMCSS válido.

Se esse atributo for definido, o leitor de origem ou o gravador de coletor registrará seus threads de processamento de áudio com a classe do MMCSS especificada. O MMCSS garante que o processamento de dados no leitor de origem ou no gravador de coletor tenha prioridade sobre outras tarefas do sistema.

Para especificar a prioridade base para threads de áudio, defina o atributo de [áudio do MF \_ ReadWrite \_ MMCSS \_ Priority \_ ](mf-readwrite-mmcss-priority-audio.md) . Se esse atributo não estiver definido, a prioridade base para threads de áudio será zero.

Esse atributo substitui o atributo de [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) para threads de processamento de áudio. Se nenhum atributo for definido, os threads de áudio não serão registrados com MCSS.

Para a maioria dos aplicativos, a falha de áudio é muito mais perceptível para o usuário do que a falha de vídeo e, portanto, menos aceitável. Por esse motivo, um aplicativo normalmente deve definir o \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ para uma classe do MMCSS de prioridade mais alta do que a [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md). Isso garante que o processamento de áudio receba prioridade mais alta do que outras tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
