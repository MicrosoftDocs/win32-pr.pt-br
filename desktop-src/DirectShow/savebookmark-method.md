---
description: O método SaveBookmark salva a posição e o estado do disco atual do objeto MSWebDVD para que o usuário possa retornar para o mesmo local posteriormente.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766261"
---
# <a name="savebookmark-method"></a>Método SaveBookmark

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SaveBookmark` método salva a posição e o estado atuais do disco do objeto **MSWebDVD** para que o usuário possa retornar para o mesmo local posteriormente.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um indicador é um instantâneo do estado atual do navegador de DVD. Isso inclui informações como o local em que ele está sendo reproduzido no disco e quais fluxos de áudio e subimagems são selecionados. Ao salvar um indicador, o usuário pode fechar o aplicativo, desligar o computador e voltar mais tarde para continuar a exibir o disco certo, onde ele parou, com todas as configurações, assim como estavam antes. Somente um indicador pode ser salvo em um determinado momento. Quando você chama `SaveBookmark` , o indicador antigo é substituído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




