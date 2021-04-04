---
title: Movendo objetos
description: Movendo objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, movendo objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007305"
---
# <a name="moving-objects"></a>Movendo objetos

Para mover um objeto em um domínio, use o método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

**Para mover um objeto dentro de um domínio**

1.  Associar à interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) do objeto a ser movido.
2.  Obtenha o ADsPath do objeto para mover da propriedade [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .
3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) do contêiner para o qual o objeto será movido.
4.  Mova o objeto com o método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

Se existir uma interface para o objeto que foi movido, a interface não será válida depois que o objeto for movido, pois o objeto de diretório que a interface representa não existe mais.

Para obter mais informações e um exemplo de código que mostra como mover um objeto, consulte [exemplo de código para mover um objeto](example-code-for-moving-an-object.md).

 

 