---
description: Constantes de intenção de imagem especificam o tipo de dados que a imagem deve representar.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes de intenção de imagem (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921072"
---
# <a name="image-intent-constants"></a>Constantes da intenção de imagem

Constantes de intenção de imagem especificam o tipo de dados que a imagem deve representar. A propriedade do scanner de tentativa de propriedade [**\_ atual de IPS \_ \_ WIA**](-wia-wiaitempropscanneritem.md) usa esses sinalizadores. Para fornecer uma intenção, combine um sinalizador de tipo de imagem pretendido com um sinalizador de tamanho/qualidade pretendido usando o operador OR. \_A intenção WIA \_ None não deve ser combinada com nenhum outro sinalizador. Observe que uma imagem não pode ser escala de cinza e cor.

Estas são constantes de tentativa de imagem válidas:



| Sinalizadores de tipo de imagem pretendidos           | Descrição                                  |
|-------------------------------------|----------------------------------------------|
| \_intenção WIA \_ nenhum                   | Valor padrão. Não Predefina nenhuma propriedade. |
| \_cor do \_ tipo de imagem da intenção WIA \_ \_     | Propriedades predefinidas para conteúdo de cores.         |
| \_tipo de imagem da intenção WIA escala de \_ \_ \_ cinza | Propriedades predefinidas para conteúdo em tons de cinza.     |
| \_texto do \_ tipo de imagem da intenção WIA \_ \_      | Propriedades predefinidas para conteúdo de texto.          |
| \_máscara do \_ tipo de imagem da intenção WIA \_ \_      | Máscara para todos os sinalizadores de tipo de imagem.        |



 



| Tamanho de imagem pretendido/sinalizadores de qualidade | Descrição                                  |
|-----------------------------------|----------------------------------------------|
| \_tamanho de \_ minimização da intenção WIA \_       | Propriedades predefinidas para minimizar o tamanho da imagem.    |
| objetivo do WIA \_ \_ maximizar \_ qualidade    | Propriedades predefinidas para maximizar a qualidade da imagem. |
| \_máscara de \_ tamanho de intenção WIA \_           | Máscara para todos os sinalizadores de tamanho/qualidade.      |
| \_ \_ melhor visualização da intenção WIA \_        | Especifica a melhor visualização de qualidade.          |



 

A lista a seguir mostra o nome da constante C/C++ seguido pelo nome correspondente entre parênteses que é usado no script. Os nomes de script são do tipo enumerado WiaIntent. Observe que nem todas as constantes estão disponíveis por meio de script.



| Constante/valor                                                                                                                                                                                                                                                                         | Descrição                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ \_Cor do \_ tipo \_ de imagem da intenção**</dt> <dt>0x00000001</dt> </dl>             | Propriedades predefinidas para conteúdo de cores.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ Tipo de imagem de intenção \_ \_ tons de \_ cinza**</dt> <dt>0x00000002</dt> </dl> | Propriedades predefinidas para conteúdo em tons de cinza.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ Tipo de imagem de intenção \_ \_ \_ texto**</dt> <dt>0x00000004</dt> </dl>                | Propriedades predefinidas para conteúdo de texto.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ 0x00010000 \_ de \_ tamanho de minimizar intenção**</dt> <dt></dt> </dl>                       | Propriedades predefinidas para minimizar o tamanho da imagem.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ INTENÇÃO \_ maximizar \_ qualidade**</dt> <dt>0x00020000</dt> </dl>              | Propriedades predefinidas para maximizar a qualidade da imagem.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ 0x00040000 de \_ melhor \_ Visualização da intenção**</dt> <dt></dt> </dl>                          | Especifica a melhor visualização de qualidade.<br/>          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




