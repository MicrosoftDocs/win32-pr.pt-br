---
description: Especifica se um quadro de vídeo desentrelaçado foi derivado do campo superior ou do campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Atributo MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761058"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>\_Atributo MFSampleExtension DerivedFromTopField

Especifica se um quadro de vídeo desentrelaçado foi derivado do campo superior ou do campo inferior. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Este atributo é válido somente para amostras desentrelaçadas. Defina esse atributo se o quadro tiver sido desentrelaçado interpolando um dos campos.

Se o valor for **true**, o campo inferior foi interpolado a partir do campo superior. Se o valor for **false**, o campo superior foi interpolado a partir do campo inferior.

Se o atributo não estiver definido, o quadro não foi desentrelaçado. O quadro é um quadro progressivo real ou é um quadro entrelaçado.

Esse atributo é informativo. Um desentrelaçador de software pode definir esse atributo. Se esse atributo for definido, ele fornecerá uma dica de que você pode recuperar o campo original descartando as linhas de digitalização interpoladas. Por exemplo, se o atributo for **true**, você poderá recuperar o campo superior original descartando o campo inferior interpolado.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> <dt>

[Entrelaçamento de vídeo](video-interlacing.md)
</dt> </dl>

 

 




