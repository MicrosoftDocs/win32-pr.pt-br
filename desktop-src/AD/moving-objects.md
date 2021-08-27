---
title: Movendo objetos
description: Movendo objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Exemplos do Active Directory do Active Directory, movendo objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1158bfc3fb85712b2ab52b6b69d86c7af52675d210b75b0c9974fc2da6359ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025854"
---
# <a name="moving-objects"></a>Movendo objetos

Para mover um objeto dentro de um domínio, use o [**método IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

**Para mover um objeto dentro de um domínio**

1.  A bind à [**interface IADs**](/windows/desktop/api/iads/nn-iads-iads) do objeto a ser movimentado.
2.  Obter o ADsPath do objeto a ser movimentado da [**propriedade IADs.ADsPath.**](/windows/desktop/ADSI/iads-property-methods)
3.  A bind à [**interface IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) do contêiner para o qual o objeto será movido.
4.  Mova o objeto com o [**método IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Se existir uma interface para o objeto que foi movido, a interface não será válida depois que o objeto for movido porque o objeto de diretório que a interface representa não existe mais.

Para obter mais informações e um exemplo de código que mostra como mover um objeto, consulte [Código de exemplo para mover um objeto](example-code-for-moving-an-object.md).

 

 