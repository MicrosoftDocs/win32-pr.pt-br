---
title: Configurando o provedor de serviços do Microsoft Locator Name
description: Você pode alterar o nome do provedor de serviços especificado editando o arquivo de configuração Rpcreg. dat, que contém os parâmetros NSP e as configurações do Protocolo RPC. Use um editor de texto para alterar as entradas NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292377"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Configurando o provedor de serviços do Microsoft Locator Name

Você pode alterar o nome do provedor de serviços especificado editando o arquivo de configuração Rpcreg. dat, que contém os parâmetros NSP e as configurações do Protocolo RPC. Use um editor de texto para alterar as entradas NSP.

**Para reconfigurar o provedor de serviços do Microsoft Locator Name**

1.  Abra o arquivo Rpcreg. dat usando um editor de texto.

    Rpcreg. dat está no diretório raiz, a menos que você tenha especificado um caminho diferente durante a instalação.

2.  Defina os valores a seguir para as entradas do registro. 

    | Entrada de registro                                         | Valor                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Protocolo de software \\ RPC da Microsoft \\ \\ NameService \\       | A sequência de protocolo para o protocolo que você está usando. O padrão é **ncacn \_ NP**.                                                                   |
    | Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress | O nome do computador que está executando o localizador que é usado por clientes durante operações de pesquisa de serviço de nome. O padrão é o controlador de domínio primário. |
    | Software \\ Microsoft \\ RPC \\ NameService \\ Endpoint       | O nome do ponto de extremidade usado pelo serviço de nome. O padrão é \\ \\ localizador de pipe.                                                                    |

    

     

3.  Salve e feche o arquivo.

 

 




