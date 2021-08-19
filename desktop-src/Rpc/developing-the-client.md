---
title: Desenvolvendo o cliente
description: Desenvolver um programa cliente RPC é semelhante ao desenvolvimento do programa de servidor. Para obter informações sobre como desenvolver um programa de servidor RPC, consulte Desenvolvendo o servidor.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, desenvolvendo o cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccc719d724ecdcc5631c5f72c5190870f864e06affd45bcce3e7f2da79fb709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021887"
---
# <a name="developing-the-client"></a>Desenvolvendo o cliente

Desenvolver um programa cliente RPC é semelhante ao desenvolvimento do programa de servidor. Para obter informações sobre como desenvolver um programa de servidor RPC, consulte [Desenvolvendo o servidor](developing-the-server.md).

Assim como no desenvolvimento de servidor, seu programa cliente deve incluir o arquivo de header que o compilador MIDL gera do arquivo .idl. O compilador MIDL também gera um arquivo de origem C que contém o stub do cliente. Você deve compilar esse arquivo de origem C e vinculá-lo ao programa cliente. (Além disso, o compilador MIDL gera um arquivo de origem C que contém o stub do servidor, mas isso não é relevante para esta discussão.)

Além de compilar e vincular o stub do cliente com seus arquivos de programa, você deve vincular a biblioteca de importação (e quaisquer outras bibliotecas que seu programa cliente precise) ao programa cliente. O processo de criação de um programa cliente RPC é ilustrado no diagrama a seguir.

![processo de criação de um programa cliente para um aplicativo distribuído](images/clntdev.png)

O exemplo na ilustração anterior demonstra a criação de um programa cliente RPC chamado MyClnt.exe. A primeira etapa é definir a interface no arquivo MyApp.idl. O compilador MIDL usa MyApp.idl para gerar o arquivo MyApp \_ c.c, que contém o stub do cliente. Ele também gera o arquivo MyApp.h, que o programa cliente deve incluir. O programa cliente também precisará incluir os arquivos RPC.h e RPCNDR.h.

O próprio programa cliente é criado no arquivo MyClnt.c. Em um projeto real, o programa cliente normalmente seria composto por vários arquivos de origem C. Todos eles precisariam ser compilados e vinculados. No entanto, este exemplo usa apenas um arquivo para simplificar.

Os arquivos MyClnt.c e MyApp c.c são compilados e vinculados junto com a biblioteca em tempo de executar RPC e quaisquer outras bibliotecas de que o programa \_ cliente precise. O resultado é um programa cliente executável chamado MyClnt.exe.

Se você não compilar seu arquivo IDL no modo de compatibilidade do OSF ([**/osf**](/windows/desktop/Midl/-osf)), o programa cliente deverá fornecer uma função para alocar memória e uma função para desalocá-lo. Para Windows 2000 e versões posteriores, o modo recomendado é [**/Oicf**](/windows/desktop/Midl/-oi). Para obter detalhes, [consulte Como a memória é alocada e desaloqueada](how-memory-is-allocated-and-deallocated.md)e [Ponteiros e Alocação de memória.](pointers-and-memory-allocation.md)

 

 