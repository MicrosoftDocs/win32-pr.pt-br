---
title: Desenvolvendo a interface
description: Uma interface RPC descreve as funções remotas que o programa do servidor implementa.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Chamada de procedimento remoto RPC, tarefas, desenvolvendo a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23829dcf143f63e791984e51194686d193d69cd575fadbc0e29c13a6f2279df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930584"
---
# <a name="developing-the-interface"></a>Desenvolvendo a interface

Uma interface RPC descreve as funções remotas que o programa do servidor implementa. A interface garante que o cliente e o servidor se comuniquem usando as mesmas regras quando o cliente chama um procedimento remoto que o servidor oferece. Uma interface consiste em um nome de interface, alguns atributos, um tipo opcional ou definições de constante e um conjunto de declarações de procedimento. Cada declaração de procedimento deve conter um nome de procedimento, tipo de retorno e lista de parâmetros.

As interfaces são definidas no linguagem IDL da Microsoft (MIDL). Se você estiver familiarizado com C ou C++, as definições de interface MIDL parecerão bastante diretas. O MIDL se assemelha a C e C++ de várias maneiras.

Ao desenvolver um aplicativo RPC, um editor de texto é usado para definir a interface e armazená-lo em um arquivo de texto com uma extensão. idl. Para obter mais informações, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md). O compilador MIDL gera um arquivo de cabeçalho que seu programa inclui nos arquivos de origem do cliente e do servidor. O compilador MIDL também gera dois arquivos de origem C. Você compila e vincula um deles ao seu programa cliente e o outro ao seu programa de servidor. Esses dois arquivos de origem do C são os stubs do cliente e do servidor. Para obter uma visão geral dos stubs do cliente e do servidor, consulte [como funciona o RPC](how-rpc-works.md). Para obter uma visão geral do compilador MIDL, consulte [Compilando um arquivo MIDL](using-midl.md).

Por padrão, o cliente e o stub do servidor têm o mesmo nome, o que pode causar problemas se o cliente for vinculado com o stub do servidor ou vice-versa. Usar a opção MIDL [**/prefix**](/windows/desktop/Midl/-prefix) impede que esse erro comum ocorra.

A ilustração a seguir mostra o processo de criação de uma interface.

![a criação de stubs de cliente e de servidor com a opção/prefix impede problemas de compilação acidentais](images/idldev.png)

É possível que você também precise especificar um arquivo de configuração de aplicativo (ACF) para entrada para o compilador MIDL também. Para obter mais informações sobre arquivos de configuração de aplicativo, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md).

Além do compilador MIDL, normalmente você precisará usar o utilitário Uuidgen para gerar um identificador exclusivo universal (UUID, intercambiável com o termo GUID). Esta seção apresenta informações sobre essas duas ferramentas, divididas nos seguintes tópicos:

-   [Gerando UUIDs de interface](generating-interface-uuids.md)
-   [Usando MIDL](using-midl.md)

 

 