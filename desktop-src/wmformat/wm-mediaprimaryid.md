---
title: WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID contém o GUID da classe de mídia primária.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato de mídia do Windows do WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823349"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

O atributo **WM/MediaClassPrimaryID** contém o GUID da classe de mídia primária.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo de Dados

**\_GUID do tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo deve ser definido como um dos valores na tabela a seguir.



| GUID de classe primária                     | Descrição                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Use para arquivos de música. Não use para áudio que não seja música. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Use para arquivos de vídeo.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Use para arquivos de áudio que não são música.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Use para arquivos que não são áudio ou vídeo.               |



 

Ao especificar um identificador de classe primário, você também deve definir um identificador de classe secundário para esclarecer o tipo de conteúdo no arquivo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




