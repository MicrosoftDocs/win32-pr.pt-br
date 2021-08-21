---
title: Impedindo vários carregamentos
description: Quando você carrega um arquivo, o BITS cria uma ID de sessão que identifica a sessão de carregamento para o cliente BITS e para o servidor BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c08555acf8bcdc99576675b0ec5852f322f7b37fea9821f3f0156352a29b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701696"
---
# <a name="preventing-multiple-uploads"></a>Impedindo vários carregamentos

Quando você carrega um arquivo, o BITS cria uma ID de sessão que identifica a sessão de carregamento para o cliente BITS e para o servidor BITS. Se a conexão entre o cliente BITS e o servidor for interrompida enquanto o BITS estiver carregando um arquivo, o cliente usará a ID de sessão para tentar retomar o carregamento.

Se o cliente BITS se conectar ao mesmo servidor que antes, o servidor reconhecerá a ID de sessão e o carregamento será retomado do ponto de interrupção. No entanto, se o cliente se conectar a um servidor diferente, o cliente deverá iniciar o carregamento desde o início, porque o novo servidor não tem o contexto de sessão ou os dados carregados anteriormente. Os BITS podem se conectar a um servidor diferente quando o servidor BITS é hospedado em um web farm e a propriedade de extensão IIS do BITS, [BITSHostId](bits-iis-extension-properties.md), não está definida. A propriedade BITSHostId impede reinicializações, forçando o cliente BITS a se conectar ao endereço exclusivo do servidor anterior, em vez do endereço do servidor compartilhado.

O servidor BITS tentará enviar o arquivo de upload apenas uma vez para o aplicativo de servidor, mas é possível que o arquivo possa ser enviado mais de uma vez. Isso pode ocorrer, por exemplo, se o servidor BITS envia o arquivo para o aplicativo de servidor e, em seguida, termina enquanto aguarda a resposta do aplicativo de servidor. O cliente BITS receberá um código de erro da camada HTTP e tentará o upload novamente após um atraso. Se o servidor ficar offline por mais tempo do que o tempo limite de [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) , o cliente eventualmente enviará a solicitação para o endereço do servidor compartilhado novamente; um servidor BITS diferente receberá o arquivo e o entregará novamente para o aplicativo do servidor.

Um caso semelhante pode ocorrer mesmo com um único servidor front-end. Por exemplo, quando o cliente carregou o arquivo inteiro no servidor, o bloco final faz com que o servidor encaminhe o arquivo para o aplicativo de servidor. Se o servidor BITS ou o aplicativo de servidor terminar depois que o arquivo for processado, mas antes que a confirmação seja enviada ao cliente, o cliente receberá um código de erro e tentará novamente mais tarde. Quando o cliente tentar novamente, o servidor BITS verá que o bloco final foi carregado, e ele encaminhará novamente o arquivo para o aplicativo de servidor. Se receber o arquivo de carregamento várias vezes for um problema para o aplicativo de servidor, você deverá considerar a inclusão de um identificador de transação nos dados.

 

 




