---
description: Executando o código de exemplo de cliente TCP/IP completo e aplicativo de servidor.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Executando o cliente Winsock e o exemplo de código do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920910"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Executando o cliente Winsock e o exemplo de código do servidor

Esta seção contém o código-fonte completo para os aplicativos de cliente e servidor TCP/IP:

-   [Código completo do cliente Winsock](complete-client-code.md)
-   [Código completo do servidor Winsock](complete-server-code.md)

O aplicativo de servidor deve ser iniciado antes do aplicativo cliente ser iniciado.

Para executar o servidor, compile o código-fonte completo do servidor e execute o arquivo executável. O aplicativo de servidor escuta na porta TCP 27015 para que um cliente se conecte. Quando um cliente se conecta, o servidor recebe dados do cliente e ecoa (envia) os dados recebidos de volta para o cliente. Quando o cliente desliga a conexão, o servidor desliga o soquete do cliente, fecha o soquete e sai.

Para executar o cliente, compile o código-fonte completo do cliente e execute o arquivo executável. O aplicativo cliente requer que o nome do computador ou endereço IP do computador em que o aplicativo do servidor está sendo executado seja passado como um parâmetro de linha de comando quando o cliente é executado. Se o cliente e o servidor forem executados no computador de exemplo, o cliente poderá ser iniciado da seguinte maneira:

**localhost do cliente**

O cliente tenta se conectar ao servidor na porta TCP 27015. Depois que o cliente se conecta, o cliente envia dados ao servidor e recebe todos os dados enviados do servidor. O cliente fecha o soquete e sai.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



