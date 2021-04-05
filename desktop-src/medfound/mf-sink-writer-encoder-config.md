---
description: Contém um ponteiro para um repositório de propriedades com propriedades de codificação.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Atributo MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662455"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>\_Atributo de \_ \_ configuração do codificador do gravador de coletor MF \_

Contém um ponteiro para um repositório de propriedades com propriedades de codificação.

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Esse atributo permite que um aplicativo defina propriedades de codificação ao usar o [gravador de coletor](sink-writer.md). Para definir esse atributo, execute as seguintes etapas:

1.  Chame [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um novo repositório de propriedades.
2.  Defina as propriedades do codificador no repositório de propriedades. As propriedades disponíveis dependem do codificador. Para obter mais informações, consulte [objetos de codec](codecobjects.md).
3.  Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.
4.  Chame [**IMFAttributes:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para definir o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) no repositório de atributos.
5.  Crie uma nova instância do gravador de coletor. Passe o ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para a função de criação. Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).

O gravador do coletor define as propriedades no codificador antes de definir os tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Atributos do gravador de coletor](sink-writer-attributes.md)
</dt> </dl>

 

 
