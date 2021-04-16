---
description: Se um computador estiver executando o Windows 2000 Server ou posterior em uma rede, os usuários poderão armazenar seus perfis no servidor. Esses perfis são chamados de perfis de usuário de roaming.
title: Perfis de usuário em roaming
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967997"
---
# <a name="roaming-user-profiles"></a>Perfis de usuário em roaming

Se um computador estiver executando o Windows 2000 Server ou posterior em uma rede, os usuários poderão armazenar seus perfis no servidor. Esses perfis são chamados de *perfis de usuário de roaming*.

Os perfis de usuário de roaming têm as seguintes vantagens:

-   Disponibilidade automática de recursos. O perfil exclusivo de um usuário fica automaticamente disponível quando ele faz logon em qualquer computador na rede. Os usuários não precisam criar um perfil em cada computador que usam em uma rede.
-   Substituição e backup simplificados do computador. Quando o computador de um usuário deve ser substituído, ele pode ser substituído facilmente, pois todas as informações de perfil do usuário são mantidas separadamente na rede, independentemente de um computador individual. Quando o usuário faz logon no novo computador pela primeira vez, a cópia de servidor do perfil do usuário é copiada para o novo computador.

O perfil do usuário não é carregado automaticamente quando o usuário faz logon usando a função [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Para carregar um perfil de usuário móvel programaticamente, use a função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Para descarregar um perfil de usuário móvel carregado por **LoadUserProfile**, chame a função [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
