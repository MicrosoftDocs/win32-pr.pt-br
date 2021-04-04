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
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="7a8e8-103">Protegendo pacotes em computadores bloqueados</span><span class="sxs-lookup"><span data-stu-id="7a8e8-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="7a8e8-104">A adesão às seguintes diretrizes ao criar um pacote de Windows Installer que será usado em computadores bloqueados ajuda a manter um ambiente seguro durante a instalação:</span><span class="sxs-lookup"><span data-stu-id="7a8e8-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="7a8e8-105">Teste seu pacote para ter compatibilidade com a [política do sistema](system-policy.md)de computador Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="7a8e8-106">Certifique-se de que o pacote seja executado com todos os [níveis de interface do usuário](user-interface-levels.md), nenhum, básico, limitado e completo.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="7a8e8-107">Teste seu pacote em partições NTFS, com privilégios [*elevados*](e-gly.md) e não elevados.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="7a8e8-108">A partir do Windows Installer 3,0, a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md) permite que usuários não administradores corrijam aplicativos instalados no contexto por máquina.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="7a8e8-109">Teste seu pacote de patch no Windows Vista e no Windows XP para instalação por usuários com acesso de administrador e por usuários não administradores.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



