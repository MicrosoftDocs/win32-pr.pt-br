---
description: Descreve o processo de uma operação de e/s de rede no Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrição de uma operação de e/s de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296809"
---
# <a name="description-of-a-network-io-operation"></a>Descrição de uma operação de e/s de rede

A figura a seguir ilustra o processo de uma operação de e/s de rede no Windows.

![operação de e/s de rede no Windows](images/fig4.png)

Quando um aplicativo chama uma função de e/s de arquivo para acessar um arquivo em um computador remoto, ocorrem os seguintes eventos:

-   A solicitação de e/s é interceptada por um [redirecionador de rede](network-redirectors.md), também chamado simplesmente de redirecionador, no computador local. Isso é descrito na figura anterior pela seta sólida entre o aplicativo e o redirecionador do cliente.
-   O redirecionador constrói um pacote de dados que contém todas as informações sobre a solicitação e a envia para o servidor onde o arquivo está localizado. Isso é descrito na figura anterior pela seta sólida entre o redirecionador do cliente e o redirecionador do servidor.
-   O redirecionador no servidor recebe o pacote do cliente, autentica o acesso ao arquivo exigido pela solicitação de e/s e, se autenticado, executa a solicitação em nome do cliente. Caso contrário, ele retorna um código de erro para o redirecionador no cliente. Isso é representado na figura anterior pela seta sólida curvada entre o redirecionador do servidor e o arquivo.
-   Quando a solicitação é executada, o redirecionador no servidor envia todos os dados resultantes da solicitação de e/s para o redirecionador no cliente, juntamente com uma notificação de êxito. Isso é descrito na figura anterior pela seta pontilhada entre o servidor e o redirecionador do cliente.
-   O redirecionador no cliente recebe o pacote do servidor e passa os dados no pacote para o aplicativo junto com uma notificação de êxito. Isso é descrito na figura anterior pela seta pontilhada entre o redirecionador do cliente e o aplicativo.

O Windows pode usar uma variedade de protocolos de rede para executar uma operação de e/s de rede, incluindo [o protocolo SMB da Microsoft e a visão geral do protocolo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Diferenças em e/s de rede e local](differences-in-local-and-network-i-o.md)<br/> | Diferenças entre e/s local e e/s de rede no Windows.<br/> |
| [Redirecionadores de rede](network-redirectors.md)<br/>                                   | Descreve a funcionalidade de um redirecionador de rede.<br/>      |



 

 

 




