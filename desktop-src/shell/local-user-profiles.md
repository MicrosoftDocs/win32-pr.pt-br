---
description: O sistema cria automaticamente um perfil de usuário local para cada usuário quando o usuário faz logon no computador pela primeira vez. O sistema mantém automaticamente as configurações do ambiente de trabalho de cada usuário em um perfil de usuário no computador local.
title: Perfis de usuário local
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968016"
---
# <a name="local-user-profiles"></a>Perfis de usuário local

A segurança do Windows requer um perfil de usuário para cada conta de usuário em um computador. O sistema cria automaticamente um *perfil de usuário local* para cada usuário quando o usuário faz logon no computador pela primeira vez. O sistema mantém automaticamente as configurações do ambiente de trabalho de cada usuário em um perfil de usuário no computador local.

Windows Vista e posterior: os perfis de usuário são gerenciados por meio do item do painel de controle de **contas de usuário** .

Windows 2000 e Windows XP: para copiar ou excluir um perfil de usuário, selecione **sistema** no painel de controle, a guia **avançado** e, em seguida, o botão **configurações** na área **perfil do usuário** .

O perfil do usuário não é carregado automaticamente quando o usuário faz logon usando a função [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Para carregar um perfil de usuário programaticamente, use a função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Para descarregar um perfil de usuário carregado pelo **LoadUserProfile**, chame a função [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
