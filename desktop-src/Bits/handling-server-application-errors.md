---
title: Manipulando erros de aplicativo do servidor
description: Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635020"
---
# <a name="handling-server-application-errors"></a>Manipulando erros de aplicativo do servidor

Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200. Se o aplicativo não retornar 200, o cliente BITS usará o código de erro para determinar se o erro é um erro transitório ou erro fatal.

Todos os códigos de erro 3xx são erros transitórios, exceto 300-305 e 307, que são erros fatais. Todos os códigos de erro 4xx são erros fatais, exceto 408 e 409, que são erros transitórios. Todos os códigos de erro 5xx são erros transitórios, exceto 501 e 505, que são erros fatais. Todos os outros códigos HTTP são considerados erros transitórios. Observe que um código de erro 403 é o único código de erro que impede que o BITS envie o arquivo de upload para o aplicativo de servidor novamente.

Para recuperar o erro, chame o método [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . O contexto de erro será um \_ aplicativo remoto de contexto de erro BG \_ \_ \_ .

 

 




