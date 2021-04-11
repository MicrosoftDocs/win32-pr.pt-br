---
description: A propriedade DVDAdm. BookmarkOnClose define ou recupera um valor que informa ao objeto MSDVDAdm se deve salvar automaticamente um indicador do local atual e as configurações quando o usuário fechar o aplicativo.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propriedade BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296034"
---
# <a name="bookmarkonclose-property"></a>Propriedade BookmarkOnClose

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm.BookmarkOnClose` propriedade define ou recupera um valor que informa ao objeto MSDVDAdm se deve salvar automaticamente um indicador do local atual e as configurações quando o usuário fechar o aplicativo.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano, que, se true, indica que o controle MSDVDAdm salvará um indicador de todas as configurações de DVD, incluindo a posição em disco, o nível pai e o país/região pai quando o usuário fechar o aplicativo de DVD Player.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de true.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



