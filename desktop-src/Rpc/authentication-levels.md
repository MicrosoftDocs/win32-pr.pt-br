---
title: Níveis de autenticação
description: O Microsoft RPC fornece vários níveis de autenticação.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cff12dae7331577da7748c2dc069bd6e7e4af6cfb1961f80d3de461930ddc3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080896"
---
# <a name="authentication-levels"></a>Níveis de autenticação

O Microsoft RPC fornece vários níveis de autenticação. Dependendo do nível de autenticação, a origem do tráfego (que a entidade de segurança enviou o tráfego) pode ser verificada quando a conexão é estabelecida, quando o cliente inicia uma nova chamada de procedimento remoto ou durante cada troca de pacotes entre o cliente e o servidor.

Mesmo quando o remetente do tráfego é verificado, a segurança ainda é fraca, uma vez que essa verificação não garante que o pacote não foi modificado ou corrompido na rota; Ele apenas verifica se o pacote veio da entidade de segurança fornecida. Para maior segurança, os aplicativos distribuídos podem definir a biblioteca de tempo de execução RPC para verificar se nenhum dos dados trocados entre o cliente e o servidor foi modificado. A Biblioteca RPC também pode criptografar o conteúdo de cada pacote antes de enviá-lo. Em geral, os aplicativos que desejam proteger seu tráfego devem usar apenas os dois últimos níveis: integridade e privacidade.

Lembre-se de que os níveis mais altos de autenticação exigem maior sobrecarga computacional. Você, como desenvolvedor, deve decidir qual é mais importante para seu aplicativo — velocidade ou segurança. A maioria dos desenvolvedores descobre que, com alguns testes de desempenho, eles podem atingir níveis de desempenho aceitáveis, mantendo a segurança adequada.

As partes do cliente e do servidor do aplicativo distribuído devem usar o mesmo nível de autenticação. Para obter uma lista de níveis de autenticação RPC, consulte [constantes de nível de autenticação](authentication-level-constants.md).

 

 




