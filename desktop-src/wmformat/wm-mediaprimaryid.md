---
title: WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID contém o GUID da classe de mídia primária.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato de mídia do Windows WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d650c15a861cdf55af07fba6d47fb416d61a56d399b855efc461cddd2f628edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027054"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

O **atributo WM/MediaClassPrimaryID** contém o GUID da classe de mídia primária.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo de Dados

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Esse atributo deve ser definido como um dos valores na tabela a seguir.



| GUID da classe primária                     | Descrição                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Use para arquivos de música. Não use para áudio que não seja música. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Use para arquivos de vídeo.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Use para arquivos de áudio que não são música.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Use para arquivos que não são áudio ou vídeo.               |



 

Ao especificar um identificador de classe primária, você também deve definir um identificador de classe secundária para esclarecer o tipo de conteúdo no arquivo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




