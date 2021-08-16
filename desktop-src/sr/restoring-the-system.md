---
title: Restaurando o sistema
description: À medida que o computador é usado ao longo do tempo, os pontos de restauração são coletados no arquivo de dados sem qualquer gerenciamento ou intervenção exigida pelo usuário.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d7e54fd12bbb05dacd0c388c1867319189924d761a43d90c6f2a9f718f26e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857516"
---
# <a name="restoring-the-system"></a>Restaurando o sistema

À medida que o computador é usado ao longo do tempo, os pontos de restauração são coletados no arquivo de dados sem qualquer gerenciamento ou intervenção exigida pelo usuário. Se o usuário precisar restaurar o sistema para um estado anterior, os pontos de restauração disponíveis serão visíveis para o usuário por meio da interface do usuário de restauração do sistema. O usuário pode escolher qualquer um desses pontos de restauração. A única maneira de acessar esse arquivo de pontos de restauração é por meio da interface do usuário de restauração do sistema e da API de restauração do sistema; Isso é para proteger a integridade dos dados e evitar alterações acidentais feitas pelo usuário, aplicativos ou outros agentes.

Para restaurar um sistema, a restauração do sistema desfaz alterações de arquivo feitas em arquivos monitorados, recapturando o estado do arquivo no momento do ponto de restauração selecionado. Em seguida, ele substitui o registro atual pelo que foi salvo para o ponto de restauração selecionado.

Para garantir que seu aplicativo tenha o comportamento desejado após uma restauração, faça o seguinte:

-   Não armazene informações no registro que impeçam o acesso do usuário a arquivos de dados pessoais ou aplicativos na restauração do sistema. Caso contrário, você deve fornecer um mecanismo pelo qual o usuário possa baixar e reinstalar os aplicativos sem precisar pagá-los novamente.
-   Use a [API de restauração do sistema](system-restore-api.md) para criar pontos de restauração significativos na instalação e na desinstalação.
-   no Windows XP, os principais binários do aplicativo a serem protegidos devem usar extensões consistentes com as usadas em Filelist.xml. Para obter mais informações, consulte [extensões de nome de arquivo monitorado](monitored-file-extensions.md). esse arquivo não é usado pelo Windows 7 e Windows Vista. Não use tipos de extensão monitorados para arquivos editáveis pelo usuário. Por exemplo, se você nomear o arquivo de dados pessoais de um usuário usando a extensão .ini, o usuário poderá perder o trabalho como resultado de uma restauração do sistema.

 

 




