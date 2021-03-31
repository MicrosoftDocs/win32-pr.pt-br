---
description: Se os dados forem coerentes, os dados no servidor e todos os clientes serão sincronizados. Um tipo de sistema de software que fornece a coerência de dados é um RCS (sistema de controle de revisão).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Coerência de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829679"
---
# <a name="data-coherency"></a>Coerência de dados

Os dados que são *coerentes* são dados que são os mesmos na rede. Em outras palavras, se os dados forem coerentes, os dados no servidor e todos os clientes serão sincronizados. Um tipo de sistema de software que fornece a coerência de dados é um RCS (sistema de controle de revisão). Esse sistema é geralmente bastante simples, com apenas um usuário com permissão para modificar um arquivo especificado de cada vez. Outras pessoas podem ler o arquivo, mas não podem alterá-lo.

O usuário que pode alterar um arquivo é dito para tê-lo verificado. O usuário, em seguida, verifica o arquivo modificado para que outras pessoas possam ver as alterações. Somente depois que o usuário tiver verificado um arquivo novamente, outro usuário poderá verificá-lo.

Um RCS requer a intervenção ativa dos usuários para operar de maneira útil. Um sistema de arquivos que opera em uma rede deve tratar o problema automaticamente.

Fornecer cache local de dados coerentes é bem simples quando você tem um thread em um cliente que acessa um arquivo pela rede por vez. No entanto, na maioria das situações, muitos threads diferentes em um ou mais computadores podem estar lendo o mesmo arquivo. Essa situação ainda é bem simples. Como os dados no arquivo são estáticos, cada computador cliente pode ter sua própria cópia local sem implicações para a coerência dos dados.

Uma situação mais comum é um thread que modifica o arquivo e muitos outros threads lendo. No momento em que uma operação de gravação ocorre, todos os caches locais desse arquivo são obsoletos. O servidor deve notificar cada cliente para abandonar seu cache. Todas as operações de leitura subsequentes para o arquivo devem ser executadas na rede.

Em outra situação comum, vários threads em um ou mais clientes de rede podem tentar gravar no mesmo arquivo. Essa situação é semelhante a uma na qual vários usuários do RCS desejam fazer alterações no mesmo arquivo. Cada usuário em sequência deve fazer check-out do arquivo, fazer alterações e, em seguida, verificar o arquivo novamente. Da mesma forma, em um esquema de cache local, o servidor deve entregar o privilégio de gravar em um arquivo em um thread de cliente por vez.

 

 



