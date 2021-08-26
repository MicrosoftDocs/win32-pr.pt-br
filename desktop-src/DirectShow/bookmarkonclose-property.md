---
description: A propriedade DVDAdm.BookmarkOnClose define ou recupera um valor que informa ao objeto MSDVDAdm se é necessário salvar automaticamente um indicador do local atual e das configurações quando o usuário fechar o aplicativo.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propriedade BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83ed0ef05e2efe7edb3b6494e8f9709b23259207af257957551077dfbbddaba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103336"
---
# <a name="bookmarkonclose-property"></a>Propriedade BookmarkOnClose

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A propriedade define ou recupera um valor que informa ao objeto MSDVDAdm se é necessário salvar automaticamente um indicador do local atual e das configurações quando o usuário fechar o `DVDAdm.BookmarkOnClose` aplicativo.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor boolano, que, se for true, indica que o controle MSDVDAdm salvará um indicador de todas as configurações de DVD, incluindo a posição no disco, no nível dos pais e no país/região dos pais quando o usuário fechar o aplicativo de player de DVD.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão true.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



