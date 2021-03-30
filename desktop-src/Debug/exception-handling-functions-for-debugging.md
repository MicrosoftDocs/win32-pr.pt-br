---
description: Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador, passando a exceção para ele. Isso é conhecido como notificação de primeira chance. Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funções de manipulação de exceção para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826088"
---
# <a name="exception-handling-functions-for-debugging"></a>Funções de manipulação de exceção para depuração

Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador, passando a exceção para ele. Isso é conhecido como *notificação de primeira chance*. Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.

Se o depurador não tratar a exceção, o sistema tentará localizar um manipulador de exceção apropriado. Se o sistema não conseguir localizar um apropriado, o sistema notificará novamente o depurador de que ocorreu uma exceção. Isso é conhecido como *notificação de última chance*. Se o depurador não tratar a exceção após a notificação de última chance, o sistema encerrará o processo que está sendo depurado.

Para obter mais informações, consulte [manipulação de exceção do depurador](debugger-exception-handling.md).

 

 



