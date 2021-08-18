---
description: Especifica se um fluxo de imagem ASF é um tipo JPEG degradante.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdf5b2633586cf4b73279a636119ac4770a5321d6bc22b5b961fa85881019b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035164"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>Atributo TOLERANTE \_ À PERDA DE IMAGEM MT \_ \_ \_ MF

Especifica se um fluxo de imagem ASF é um tipo JPEG degradante.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica ao tipo de mídia para fluxos de imagem no ASF. Se o valor for **TRUE,** o fluxo será um tipo de imagem JPEG degradante. Caso contrário, o fluxo será um tipo de imagem JFIF. Para obter mais informações sobre esses tipos de fluxo, consulte a especificação do ASF.

Além do atributo TOLERANTE À PERDA DE IMAGEM MT MT, o tipo de mídia para um \_ \_ fluxo de imagem \_ \_ ASF contém os seguintes atributos:



| Atributo                                                 | Descrição                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | Contém o valor **imagem \_ MFMediaType**. |
| [**TAMANHO DO \_ QUADRO MT MF \_ \_**](mf-mt-frame-size-attribute.md) | Fornece o tamanho da imagem em pixels.            |



 

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




