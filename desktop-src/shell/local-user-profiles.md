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
ms.openlocfilehash: 713adc7db522ff473de42a3ecaa2a1a0671f95ee5f4039f0039a196304c7aa4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220151"
---
# <a name="local-user-profiles"></a>Perfis de usuário local

Windows segurança requer um perfil de usuário para cada conta de usuário em um computador. O sistema cria automaticamente um *perfil de usuário local* para cada usuário quando o usuário faz logon no computador pela primeira vez. O sistema mantém automaticamente as configurações do ambiente de trabalho de cada usuário em um perfil de usuário no computador local.

Windows Vista e posterior: os perfis de usuário são gerenciados por meio do item do painel de controle de **contas de usuário** .

Windows 2000 e Windows XP: para copiar ou excluir um perfil de usuário, selecione **sistema** no painel de controle, na guia **avançado** e no botão **Configurações** na área perfil de **usuário** .

O perfil do usuário não é carregado automaticamente quando o usuário faz logon usando a função [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Para carregar um perfil de usuário programaticamente, use a função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Para descarregar um perfil de usuário carregado pelo **LoadUserProfile**, chame a função [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
