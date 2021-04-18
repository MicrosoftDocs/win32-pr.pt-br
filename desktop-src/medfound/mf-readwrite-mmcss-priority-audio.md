---
description: Define a prioridade base para threads de processamento de áudio criados pelo leitor de origem ou gravador de coletor.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Atributo MF_READWRITE_MMCSS_PRIORITY_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789371"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>Atributo de áudio do MF \_ ReadWrite \_ MMCSS \_ Priority \_

Define a prioridade base para threads de processamento de áudio criados pelo leitor de origem ou gravador de coletor.

## <a name="data-type"></a>Tipo de dados

**INT32** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md). Se você definir esse atributo, defina também o atributo de [ \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) . Caso contrário, esse atributo será ignorado.

Quando o leitor de origem ou o gravador de coletor registra threads de processamento de áudio com o [serviço de Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md), o valor desse atributo especifica a prioridade de thread base. Se esse atributo não for definido, o valor padrão será zero.

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

 

 
