---
description: Para ajudar a manter uma instalação de software segura em computadores bloqueados, siga estas diretrizes ao criar o pacote de Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protegendo pacotes em computadores bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828987"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protegendo pacotes em computadores bloqueados

A adesão às seguintes diretrizes ao criar um pacote de Windows Installer que será usado em computadores bloqueados ajuda a manter um ambiente seguro durante a instalação:

-   Teste seu pacote para ter compatibilidade com a [política do sistema](system-policy.md)de computador Windows Installer.
-   Certifique-se de que o pacote seja executado com todos os [níveis de interface do usuário](user-interface-levels.md), nenhum, básico, limitado e completo.
-   Teste seu pacote em partições NTFS, com privilégios [*elevados*](e-gly.md) e não elevados.
-   A partir do Windows Installer 3,0, a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md) permite que usuários não administradores corrijam aplicativos instalados no contexto por máquina. Teste seu pacote de patch no Windows Vista e no Windows XP para instalação por usuários com acesso de administrador e por usuários não administradores.

 

 



