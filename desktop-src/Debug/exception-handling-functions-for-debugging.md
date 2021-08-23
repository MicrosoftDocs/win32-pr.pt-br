---
description: Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador passando a exceção para ela. Isso é conhecido como notificação de primeira chance. Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funções de tratamento de exceção para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4542b6e1d3ad2699b3cb43d15e327d26156760980188555b1a4bf9c68e9a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573166"
---
# <a name="exception-handling-functions-for-debugging"></a>Funções de tratamento de exceção para depuração

Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador passando a exceção para ela. Isso é conhecido como *notificação de primeira chance.* Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.

Se o depurador não tratar a exceção, o sistema tentará localizar um manipulador de exceção apropriado. Se o sistema não puder localizar um apropriado, o sistema notifica novamente o depurador de que ocorreu uma exceção. Isso é conhecido como *notificação de última chance.* Se o depurador não tratar a exceção após a notificação de última chance, o sistema encerrará o processo que está sendo depurado.

Para obter mais informações, consulte [Tratamento de exceção do depurador](debugger-exception-handling.md).

 

 



