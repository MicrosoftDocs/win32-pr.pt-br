---
title: Registrando aplicativos COM
description: Registrando aplicativos COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63caaba090c38e5917e6c85884fdf5a76e2353f6a57527ad5870d0fbd984b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129978"
---
# <a name="registering-com-applications"></a>Registrando aplicativos COM

O registro é um banco de dados do sistema que contém informações sobre a configuração de hardware e software do sistema, bem como sobre os usuários do sistema. qualquer programa baseado em Windows pode adicionar informações ao registro e ler informações de volta do registro. Os clientes pesquisam no registro os componentes interessantes a serem usados.

O registro mantém informações sobre todos os objetos COM instalados no sistema. Sempre que um aplicativo cria uma instância de um componente COM, o registro é consultado para resolver o CLSID ou ProgID do componente no nome do caminho da DLL do servidor ou do EXE que o contém. depois de determinar o servidor do componente, Windows carrega o servidor no espaço de processo do aplicativo cliente (componentes em processo) ou inicia o servidor em seu próprio espaço de processo (servidores locais e remotos). O servidor cria uma instância do componente e retorna ao cliente uma referência a uma das interfaces do componente.

para obter mais informações sobre o registro de Windows, consulte os seguintes tópicos:

-   [Hierarquia do registro](registry-hierarchy.md)
-   [Classes e servidores](classes-and-servers.md)
-   [Classificando componentes](classifying-components.md)
-   [Usando OleView](using-oleview.md)
-   [Registrando componentes](registering-components.md)
-   [Verificando registro](checking-registration.md)
-   [Tipos de usuário desconhecidos](unknown-user-types.md)
-   [Chaves do registro COM](com-registry-keys.md)

 

 




