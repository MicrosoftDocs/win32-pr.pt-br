---
title: Interface IWMPMetadataPicture (VB e C) (WMP. h)
description: Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB e C) interface do Windows Media Player
- IWMPMetadataPicture (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810545"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interface IWMPMetadataPicture (VB e C#)

Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo de metadados do [**WM/Picture**](/windows/desktop/wmformat/wmpicture). Esse atributo corresponde a imagens de arte do álbum contidas em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.

A interface **IWMPMetadataPicture** expõe as propriedades a seguir.



| Propriedade                                                                                   | Descrição                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descrição**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtém a descrição da imagem representada pelo atributo de metadados.  |
| [**MIME**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtém o tipo MIME da imagem representada pelo atributo de metadados.    |
| [**TipoDeFigura**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Obtém o tipo de imagem da imagem representada pelo atributo de metadados. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Somente para uso interno.                                                        |



 

Obtenha uma interface **IWMPMetadataPicture** passando o nome do atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) para o método a seguir e convertendo o objeto retornado.



| Interface                                  | Propriedade                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Membros

A interface **IWMPMetadataPicture (VB e C#)** não define nenhum membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

