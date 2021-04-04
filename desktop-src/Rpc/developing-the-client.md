---
title: Desenvolvendo o cliente
description: O desenvolvimento de um programa cliente RPC é semelhante ao desenvolvimento do programa do servidor. Para obter informações sobre como desenvolver um programa de servidor RPC, consulte desenvolvendo o servidor.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- Chamada de procedimento remoto RPC, tarefas, desenvolvimento do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917584"
---
# <a name="developing-the-client"></a>Desenvolvendo o cliente

O desenvolvimento de um programa cliente RPC é semelhante ao desenvolvimento do programa do servidor. Para obter informações sobre como desenvolver um programa de servidor RPC, consulte [desenvolvendo o servidor](developing-the-server.md).

Como no desenvolvimento de servidor, o programa cliente deve incluir o arquivo de cabeçalho que o compilador MIDL gera de seu arquivo. idl. O compilador MIDL também gera um arquivo de origem C contendo o stub do cliente. Você deve compilar esse arquivo de origem C e vinculá-lo ao seu programa cliente. (Além disso, o compilador MIDL gera um arquivo de origem C contendo o stub do servidor, mas isso não é relevante para essa discussão.)

Além de compilar e vincular o stub do cliente com os arquivos de programa, você deve vincular a biblioteca de importação (e todas as outras bibliotecas de que seu programa cliente precisa) ao seu programa cliente. O processo de criação de um programa cliente RPC é ilustrado no diagrama a seguir.

![processo de criação de um programa cliente para um aplicativo distribuído](images/clntdev.png)

O exemplo na ilustração anterior demonstra a criação de um programa cliente RPC chamado MyClnt.exe. A primeira etapa é definir a interface no arquivo MyApp. idl. O compilador MIDL usa MyApp. idl para gerar o arquivo MyApp \_ c. c, que contém o stub do cliente. Ele também gera o arquivo MyApp. h, que o programa cliente deve incluir. O programa cliente também precisará incluir os arquivos RPC. h e RPCNDR. h.

O próprio programa cliente é criado no arquivo MyClnt. c. Em um projeto real, o programa cliente normalmente seria composto por vários arquivos de origem C. Todos eles precisariam ser compilados e vinculados juntos. No entanto, este exemplo usa apenas um arquivo para simplificar.

Os arquivos MyClnt. c e MyApp \_ c. c são compilados e vinculados junto com a biblioteca de tempo de execução RPC e quaisquer outras bibliotecas que o programa cliente precisa. O resultado é um programa cliente executável chamado MyClnt.exe.

Se você não compilar o arquivo IDL no modo de compatibilidade uso ([**/OSF**](/windows/desktop/Midl/-osf)), o programa cliente deverá fornecer uma função para alocar memória e uma função para desalocá-lo. Para o Windows 2000 e versões posteriores, o modo recomendado é [**/Oicf**](/windows/desktop/Midl/-oi). Para obter detalhes, consulte [como a memória é alocada e desalocada](how-memory-is-allocated-and-deallocated.md), e [ponteiros e alocação de memória](pointers-and-memory-allocation.md).

 

 