---
description: Contém propriedades de configuração para um codificador.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Atributo MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722501"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>\_Atributo de \_ perfil de codificador de MFT preferencial \_

Contém propriedades de configuração para um codificador.

## <a name="data-type"></a>Tipo de dados

**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Aplica-se a

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no objeto de ativação retornado pela função [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . O atributo se aplica somente quando o objeto de ativação é configurado para criar um codificador. O valor do atributo é um ponteiro para um repositório de atributos, que contém propriedades a serem definidas no codificador.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




