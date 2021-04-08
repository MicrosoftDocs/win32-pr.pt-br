---
description: Especifica se um fluxo de imagem ASF é um tipo de JPEG degradado.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Atributo MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827203"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>\_ \_ \_ Atributo tolerante a perda de imagem MF MT \_

Especifica se um fluxo de imagem ASF é um tipo de JPEG degradado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica ao tipo de mídia para fluxos de imagem no ASF. Se o valor for **true**, o fluxo será um tipo de imagem JPEG degradado. Caso contrário, o fluxo é um tipo de imagem JFIF. Para obter mais informações sobre esses tipos de fluxo, consulte a especificação do ASF.

Além do \_ atributo de tolerância a perda de imagem MF MT \_ \_ \_ , o tipo de mídia para um fluxo de imagem ASF contém os seguintes atributos:



| Atributo                                                 | Descrição                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | Contém a **\_ imagem** do valor MFMediaType. |
| [**\_tamanho do \_ quadro MF MT \_**](mf-mt-frame-size-attribute.md) | Retorna o tamanho da imagem em pixels.            |



 

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




