---
description: Especifica se o coletor de amostra de exemplo usa o relógio de apresentação para agendar exemplos.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Atributo MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771383"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>\_Atributo de \_ relógio de ignorar SAMPLEGRABBERSINK MF \_

Especifica se o coletor de amostra de exemplo usa o relógio de apresentação para agendar exemplos.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no objeto de ativação criado pela função [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Defina o atributo antes de chamar o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto de ativação.

Por padrão, quando o coletor de amostra de exemplo recebe um exemplo, ele aguarda até que o tempo de apresentação do exemplo invoque o retorno de chamada do aplicativo. Se o \_ atributo de relógio MF SAMPLEGRABBERSINK \_ ignorar \_ for diferente de zero, o coletor de apoio de exemplo ignorará o relógio de apresentação e invocará o retorno de chamada assim que receber cada exemplo.

Uso recomendado:

-   Se você quiser processar amostras o mais rápido possível, defina esse atributo como **true**.
-   Se você quiser que as chamadas para o método de retorno de chamada sejam sincronizadas com o relógio, não defina esse atributo ou defina-o como **false**. Você pode obter amostras levemente antes do relógio, enquanto ainda permaneceu sincronizado, definindo o atributo de [**\_ deslocamento de \_ \_ tempo \_ de exemplo SAMPLEGRABBERSINK MF**](mf-samplegrabbersink-sample-time-offset-attribute.md) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




