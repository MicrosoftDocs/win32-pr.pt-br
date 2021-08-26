---
title: Manipulando erros de aplicativo do servidor
description: Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005276"
---
# <a name="handling-server-application-errors"></a>Manipulando erros de aplicativo do servidor

Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200. Se o aplicativo não retornar 200, o cliente BITS usará o código de erro para determinar se o erro é um erro transitório ou erro fatal.

Todos os códigos de erro 3xx são erros transitórios, exceto 300-305 e 307, que são erros fatais. Todos os códigos de erro 4xx são erros fatais, exceto 408 e 409, que são erros transitórios. Todos os códigos de erro 5xx são erros transitórios, exceto 501 e 505, que são erros fatais. Todos os outros códigos HTTP são considerados erros transitórios. Observe que um código de erro 403 é o único código de erro que impede que o BITS envie o arquivo de upload para o aplicativo de servidor novamente.

Para recuperar o erro, chame o método [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . O contexto de erro será um \_ aplicativo remoto de contexto de erro BG \_ \_ \_ .

 

 




