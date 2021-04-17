---
description: Contém o valor de mérito de um codec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Atributo MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754895"
---
# <a name="mft_codec_merit_attribute-attribute"></a>\_Atributo de \_ atributo mérito de codec de MFT \_

Contém o valor de mérito de um codec de hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo é definido no objeto de ativação para uma Media Foundation transformação (MFT) que representa um codec de hardware. O valor do atributo é o valor de mérito do codec.

Esse atributo controla a ordem na qual a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera codecs, se o sinalizador **\_ \_ \_ SORTANDFILTER do sinalizador de enumeração de MFT** estiver definido. MFTs com um valor de mérito aparece mais alto na lista que outros MFTs.

Este atributo não contém um valor confiável. Para verificar o valor do mérito real do codec, chame a função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .

Se o valor do atributo de \_ atributo de mérito do codec MFT \_ \_ não corresponder ao valor de mérito recuperado por [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhará e retornará um **mérito de \_ codec MF e \_ inválido \_ \_**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




