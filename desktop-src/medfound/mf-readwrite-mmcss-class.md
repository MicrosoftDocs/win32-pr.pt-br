---
description: Especifica uma classe de serviço do Agendador de classes de multimídia (MMCSS) para o leitor de origem ou o gravador de coletor.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Atributo MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663014"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>\_Atributo de classe MF ReadWrite \_ MMCSS \_

Especifica uma classe de [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para o leitor de origem ou o gravador de coletor.

## <a name="data-type"></a>Tipo de dados

**LPWSTR**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Opcionalmente, defina esse atributo ao criar uma instância do [leitor de fonte](source-reader.md) ou do [gravador de coletor](sink-writer.md). O valor do atributo deve ser um nome de classe do MMCSS válido.

Se esse atributo for definido, o leitor de origem ou o gravador do coletor registrará todos os seus threads com a classe do MMCSS especificada. O MMCSS garante que o processamento de dados no leitor de origem ou no gravador de coletor tenha prioridade sobre outras tarefas do sistema.

Para especificar a prioridade base, defina o atributo de [ \_ \_ \_ prioridade MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) . Se esse atributo não estiver definido, a prioridade base será zero.

Para threads de processamento de áudio, o atributo de [ \_ áudio da classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) (se definido) substitui esse atributo.

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

 

 
