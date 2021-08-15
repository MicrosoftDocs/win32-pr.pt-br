---
description: Define a prioridade de thread base para o leitor de origem ou o gravador de coletor.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Atributo MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740598"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
