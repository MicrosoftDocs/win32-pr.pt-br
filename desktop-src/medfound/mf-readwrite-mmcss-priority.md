---
description: Define a prioridade de thread base para o leitor de origem ou o gravador de coletor.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Atributo MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011699"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>\_Atributo de prioridade MF ReadWrite \_ MMCSS \_

Define a prioridade de thread base para o leitor de origem ou o gravador de coletor.

## <a name="data-type"></a>Tipo de dados

**INT32** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md). Se você definir esse atributo, defina também o atributo de [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) . Caso contrário, esse atributo será ignorado.

Quando o leitor de origem ou o gravador de coletor registra threads com o [serviço de Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md), o valor desse atributo especifica a prioridade de thread base. Se esse atributo não for definido, o valor padrão será zero.

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

 

 
