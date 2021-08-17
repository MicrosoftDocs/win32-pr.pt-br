---
title: Interface IWMPMetadataPicture (VB e C) (WMP. h)
description: Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- Windows Media Player de interface IWMPMetadataPicture (VB e C)
- Windows Media Player de interface IWMPMetadataPicture (VB e C), descrita
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
ms.openlocfilehash: 1b73a48b2ea93d696f2b8780edec90dfcf0522e2353c508e31d96dd7a404d0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996486"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interface IWMPMetadataPicture (VB e C#)

Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo de metadados do [**WM/Picture**](/windows/desktop/wmformat/wmpicture). Esse atributo corresponde a imagens de arte do álbum contidas em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.

A interface **IWMPMetadataPicture** expõe as propriedades a seguir.



| Propriedade                                                                                   | Descrição                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descrição**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtém a descrição da imagem representada pelo atributo de metadados.  |
| [**Tipo MIME**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtém o tipo MIME da imagem representada pelo atributo de metadados.    |
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

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

