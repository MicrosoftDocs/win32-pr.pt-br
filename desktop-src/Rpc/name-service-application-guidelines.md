---
title: Diretrizes de aplicativo de serviço de nome
description: Ao desenvolver seu aplicativo distribuído, você precisa fornecer aos usuários do aplicativo um método para especificar o nome sob o qual eles podem registrar o aplicativo no banco de dados do serviço de nome.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e0e79f8ddb9e2076da8d7b8d2c275cb1b1941f6867bfea68dd46bc6c352d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927825"
---
# <a name="name-service-application-guidelines"></a>Diretrizes de aplicativo de serviço de nome

Ao desenvolver seu aplicativo distribuído, você precisa fornecer aos usuários do aplicativo um método para especificar o nome sob o qual eles podem registrar o aplicativo no banco de dados do serviço de nome. Esse método pode consistir em um arquivo de dados, uma entrada de linha de comando ou uma caixa de diálogo.

Embora a arquitetura de serviço de nome RPC dê suporte a vários métodos para organizar as entradas de servidor de um aplicativo, ele é otimizado para pesquisas. Como resultado, as atualizações frequentes podem prejudicar o desempenho do serviço de nome e do aplicativo. Para evitar a exportação de informações desnecessariamente, escolha um design que permita que o servidor determine se suas informações estão no banco de dados do serviço de nome. Além disso, cada instância de servidor deve exportar para seu próprio nome de entrada. Caso contrário, será difícil para uma instância alterar seus UUIDs de objeto com suporte ou sequências de protocolo sem perturbar as informações de outra instância.

O método a seguir evita essas armadilhas e fornece um bom desempenho, não importa qual serviço de nome sua rede usa.

Para começar, crie seu aplicativo de forma que, na primeira vez que uma determinada instância de servidor for iniciada, ele escolha um nome de entrada de servidor exclusivo e salve esse nome no registro junto com as outras informações de configuração do aplicativo. Em seguida, exporte seus identificadores de associação e UUIDs de objeto, se houver, para sua entrada de serviço de nome.

As invocações subsequentes da instância de servidor devem verificar se a entrada de serviço de nome está presente e contém o conjunto correto de UUIDs de objeto e identificadores de associação. Uma entrada ausente pode significar que um administrador a removeu ou que uma queda de energia fez com que as informações do serviço de nome sejam perdidas. É importante verificar se os identificadores de associação na entrada estão corretos; se um administrador adicionar suporte a TCP/IP a um computador, por exemplo, os servidores RPC escutarão nessa sequência de protocolo quando chamarem [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). No entanto, se o servidor não atualizar a entrada de serviço de nome, os clientes não serão informados de que há suporte para TCP.

Quando o cliente importa, ele deve especificar **NULL** como o nome da entrada. A especificação de **NULL** faz com que a Biblioteca RPC da Microsoft funcione para pesquisar a interface em todas as entradas de serviço de nome no domínio ou grupo de trabalho do computador cliente, localizando assim as informações para cada instância.

Se você usar UUIDs de objeto para representar objetos conhecidos, como impressoras, poderá usar uma variação desse método. Em vez de exportar associações para uma entrada, crie seu aplicativo para que cada instância crie uma entrada para cada objeto com suporte, como "/.:/ impressoras/Laser1 "e"/.:/ impressoras/Laser2. " Em seguida, faça com que o servidor exporte seus identificadores de associação para cada entrada de servidor, juntamente com o UUID do objeto relevante para essa entrada.

Nesse caso, um cliente pode procurar um recurso por nome importando da entrada de servidor relevante; Ele não requer o UUID do objeto do recurso. Se ele tiver o UUID do recurso, mas não o nome, ele poderá importar da entrada **NULL** .

 

 




