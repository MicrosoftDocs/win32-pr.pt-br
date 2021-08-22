---
description: O método SaveBookmark salva a posição atual do disco e o estado do objeto MSWebDVD para que o usuário possa retornar ao mesmo local mais tarde.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072710"
---
# <a name="savebookmark-method"></a>Método SaveBookmark

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método salva a posição atual do disco e o estado do objeto `SaveBookmark` **MSWebDVD** para que o usuário possa retornar ao mesmo local mais tarde.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um indicador é um instantâneo do estado atual do Navegador de DVD. Isso inclui informações como onde ele está sendo gravado no disco e quais fluxos de áudio e subtípicos são selecionados. Ao salvar um indicador, o usuário pode fechar o aplicativo, desligar o computador e voltar mais tarde para continuar exibindo o disco exatamente de onde ele parava, com todas as configurações exatamente como antes. Somente um indicador pode ser salvo a qualquer momento. Quando você chama `SaveBookmark` , o indicador antigo é substituído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




