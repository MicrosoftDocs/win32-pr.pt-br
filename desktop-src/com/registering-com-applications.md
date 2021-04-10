---
title: Registrando aplicativos COM
description: Registrando aplicativos COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292641"
---
# <a name="registering-com-applications"></a>Registrando aplicativos COM

O registro é um banco de dados do sistema que contém informações sobre a configuração de hardware e software do sistema, bem como sobre os usuários do sistema. Qualquer programa baseado no Windows pode adicionar informações ao registro e ler as informações do registro. Os clientes pesquisam no registro os componentes interessantes a serem usados.

O registro mantém informações sobre todos os objetos COM instalados no sistema. Sempre que um aplicativo cria uma instância de um componente COM, o registro é consultado para resolver o CLSID ou ProgID do componente no nome do caminho da DLL do servidor ou do EXE que o contém. Depois de determinar o servidor do componente, o Windows carrega o servidor no espaço de processo do aplicativo cliente (componentes em processo) ou inicia o servidor em seu próprio espaço de processo (servidores locais e remotos). O servidor cria uma instância do componente e retorna ao cliente uma referência a uma das interfaces do componente.

Para obter mais informações sobre o registro do Windows, consulte os seguintes tópicos:

-   [Hierarquia do registro](registry-hierarchy.md)
-   [Classes e servidores](classes-and-servers.md)
-   [Classificando componentes](classifying-components.md)
-   [Usando OleView](using-oleview.md)
-   [Registrando componentes](registering-components.md)
-   [Verificando registro](checking-registration.md)
-   [Tipos de usuário desconhecidos](unknown-user-types.md)
-   [Chaves do registro COM](com-registry-keys.md)

 

 




