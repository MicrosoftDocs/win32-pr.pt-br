---
description: O nome da coluna reservada \_ RowState representa o estado não persistente associado a cada linha da tabela em uma tabela de banco de dados do instalador.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146089"
---
# <a name="_rowstate-column"></a>\_Coluna RowState

O nome da coluna reservada \_ RowState representa o estado não persistente associado a cada linha da tabela em uma tabela de banco de dados do instalador. A pseudo coluna é do tipo [inteiro](integer.md)e o valor consiste em um conjunto de sinalizadores de bit. Todos os bits são legíveis, mas somente os bits UserInfo e temporários podem ser definidos. Esses dados só estarão disponíveis se as tabelas estiverem bloqueadas ou em uso (ou seja, enquanto houver uma exibição contendo as tabelas). A tabela a seguir mostra os atributos que uma linha pode ter.



| Nome           | Valor | Significado                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | O atributo é para uso externo. Esse valor pode ser atualizado.  |
| iraTemporary   | 0x02  | A linha não é persistente. Esse valor pode ser atualizado.          |
| iraModified    | 0x04  | Uma linha foi atualizada.                                        |
| iraInserted    | 0x08  | Uma linha foi inserida.                                       |
| iraMergeFailed | 0x0F  | Foi feita uma tentativa de mesclagem com dados não idênticos e não importantes. |



 

Os bits 6 a 8 são reservados.

 

 



