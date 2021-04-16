---
description: Embora um&\# 160; contexto de reconhecedor&\# 160; não possa ser acessado em dois threads simultaneamente pela plataforma do Tablet PC, a função AdviseInkChange pode ser chamada a qualquer momento em qualquer thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considerações de Threading do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765301"
---
# <a name="recognizer-threading-considerations"></a>Considerações de Threading do reconhecedor

Embora um [contexto de reconhecedor](hrecocontext-handle.md) não possa ser acessado em dois threads simultaneamente pela plataforma do Tablet PC, a função [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) pode ser chamada a qualquer momento em qualquer thread. Como a plataforma Tablet PC não garante que haja apenas um contexto de reconhecedor por vez, dois contextos de reconhecedor separados em threads separados podem tentar acessar simultaneamente o [reconhecedor](hrecognizer-handle.md). Portanto, as variáveis globais em seu mecanismo de reconhecimento devem ser thread-safe.

As listas de palavras são uma implementação opcional usada para aumentar a precisão. Se o reconhecedor implementar listas de palavras, ele deverá ser thread-safe. Para obter mais informações sobre como usar listas de palavras, consulte [usando dicionários de aplicativos](using-application-dictionaries.md).

Para obter detalhes sobre outras considerações sobre Threading, consulte [considerações de Threading do Tablet PC](tablet-pc-threading-considerations.md).

 

 



