---
description: A propriedade DVDAdm. BookmarkOnStop define ou recupera um valor que informa ao objeto MSWebDVD se é para salvar automaticamente um indicador do local e das configurações atuais quando o usuário clica no botão parar.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propriedade BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73d8b9829075125437e05da96c78d101f5a7f5df4dc2decc25f044cc3f5f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662668"
---
# <a name="bookmarkonstop-property"></a>Propriedade BookmarkOnStop

A `DVDAdm.BookmarkOnStop` propriedade define ou recupera um valor que informa ao objeto MSWebDVD se é para salvar automaticamente um indicador do local e das configurações atuais quando o usuário clica no botão **parar** .

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se o objeto MSDVDAdm salvará um indicador de todas as configurações de DVD, incluindo a posição em disco, o nível pai e o país/região pai.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de false.

Indicadores são válidos somente para um determinado computador. Um usuário não pode salvar um indicador e, em seguida, enviá-lo para outra pessoa para ler em um computador diferente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



