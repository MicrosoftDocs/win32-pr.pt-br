---
description: Descreve o processo de uma operação de E/S de rede em Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrição de uma operação de E/S de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d872f8eaf6f9a90ab313e6a7b17e3fe93073cdb13e5b039e401de41287f1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150813"
---
# <a name="description-of-a-network-io-operation"></a>Descrição de uma operação de E/S de rede

A figura a seguir ilustra o processo de uma operação de E/S de rede em Windows.

![operação de E/S de rede em janelas](images/fig4.png)

Quando um aplicativo chama uma função de E/S de arquivo para acessar um arquivo em um computador remoto, os seguintes eventos ocorrem:

-   A solicitação de E/S é interceptada por um [redirecionador](network-redirectors.md)de rede , também conhecido simplesmente como redirecionador, no computador local. Isso é ilustrado na figura anterior pela seta sólida entre o aplicativo e o redirecionador de cliente.
-   O redirecionador constrói um pacote de dados que contém todas as informações sobre a solicitação e a envia para o servidor onde o arquivo está localizado. Isso é ilustrado na figura anterior pela seta sólida entre o redirecionador de cliente e o redirecionador de servidor.
-   O redirecionador no servidor recebe o pacote do cliente, autentica o acesso ao arquivo exigido pela solicitação de E/S e, se autenticado, executa a solicitação em nome do cliente. Caso não seja, ele retornará um código de erro para o redirecionador no cliente. Isso é ilustrado na figura anterior pela seta sólida curvada entre o redirecionador de servidor e o arquivo.
-   Quando a solicitação tiver sido executada, o redirecionador no servidor enviará todos os dados resultantes da solicitação de E/S para o redirecionador no cliente junto com uma notificação de êxito. Isso é ilustrado na figura anterior pela seta pontilhada entre o servidor e o redirecionador de cliente.
-   O redirecionador no cliente recebe o pacote do servidor e passa os dados no pacote para o aplicativo junto com uma notificação de êxito. Isso é ilustrado na figura anterior pela seta pontilhada entre o redirecionador de cliente e o aplicativo.

Windows pode usar uma variedade de protocolos de rede para executar uma operação de E/S de rede, incluindo o Protocolo SMB da Microsoft e a Visão geral do protocolo [CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Diferenças na E/S local e de rede](differences-in-local-and-network-i-o.md)<br/> | Diferenças entre E/S local e E/S de rede Windows.<br/> |
| [Redirecionadores de rede](network-redirectors.md)<br/>                                   | Descreve a funcionalidade de um redirecionador de rede.<br/>      |



 

 

 




