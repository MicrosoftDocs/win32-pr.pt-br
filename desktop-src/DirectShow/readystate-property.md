---
description: A propriedade ReadyState recupera o ReadyState do objeto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propriedade ReadyState (Ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: 029798e66d8ed69dc18bbb23dafc8b047d770f1bc91ac1b86ca7bdb09963c2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072780"
---
# <a name="readystate-property"></a>Propriedade ReadyState

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `ReadyState` propriedade recupera o ReadyState do objeto **MSWebDVD** .

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o ReadyState do controle.



| Código de retorno | Descrição                                               |
|-------------|-----------------------------------------------------------|
| 0           | Estado de inicialização padrão.                             |
| 1           | O objeto está carregando suas propriedades.                         |
| 2           | O objeto foi inicializado.                              |
| 3           | O objeto é interativo, mas nem todos os seus dados estão disponíveis. |
| 4           | O objeto recebeu todos os seus dados.                         |



 

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão.

Qualquer objeto inserido em uma página da Web expõe a `ReadyState` propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



 

 




