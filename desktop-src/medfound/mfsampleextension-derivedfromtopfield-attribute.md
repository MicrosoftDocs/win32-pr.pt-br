---
description: Especifica se um quadro de vídeo desintercalado foi derivado do campo superior ou do campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 376cc499dd76702abb4c7054014a7c720118f33a732856202c4e654992c30985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241186"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>Atributo MFSampleExtension \_ DerivedFromTopField

Especifica se um quadro de vídeo desintercalado foi derivado do campo superior ou do campo inferior. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Esse atributo é válido apenas para amostras desintercaladas. De definir esse atributo se o quadro foi desinteressado interpolando um dos campos.

Se o valor for **TRUE,** o campo inferior foi interpolado do campo superior. Se o valor for **FALSE,** o campo superior foi interpolado do campo inferior.

Se o atributo não estiver definido, o quadro não foi desintercalado. O quadro é um quadro progressivo verdadeiro ou é um quadro entrelaçado.

Esse atributo é informacional. Um desinterdor de software pode definir esse atributo. Se esse atributo for definido, ele fornece uma dica de que você pode recuperar o campo original, soltando as linhas de verificação interpoladas. Por exemplo, se o atributo for **TRUE,** você poderá recuperar o campo superior original, soltando o campo inferior interpolado.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> <dt>

[Entrelaçamento de vídeo](video-interlacing.md)
</dt> </dl>

 

 




