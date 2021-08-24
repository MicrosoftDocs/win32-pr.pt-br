---
description: para ajudar a manter uma instalação de software segura em computadores bloqueados, siga estas diretrizes ao criar o pacote de Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protegendo pacotes em computadores bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315296"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protegendo pacotes em computadores bloqueados

a adesão às seguintes diretrizes ao criar um pacote de Windows Installer que será usado em computadores bloqueados ajuda a manter um ambiente seguro durante a instalação:

-   teste seu pacote para ter compatibilidade com a [política do sistema](system-policy.md)de computador Windows Installer.
-   Certifique-se de que o pacote seja executado com todos os [níveis de interface do usuário](user-interface-levels.md), nenhum, básico, limitado e completo.
-   Teste seu pacote em partições NTFS, com privilégios [*elevados*](e-gly.md) e não elevados.
-   a partir do Windows Installer 3,0, a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md) permite que usuários não administradores corrijam aplicativos instalados no contexto por máquina. teste seu pacote de patch no Windows Vista e Windows XP para instalação por usuários com acesso de administrador e por usuários não administradores.

 

 



