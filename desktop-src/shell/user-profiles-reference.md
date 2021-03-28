---
description: Os seguintes elementos de API são usados com perfis de usuário.
title: Referência de perfis de usuário
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968190"
---
# <a name="user-profiles-reference"></a>Referência de perfis de usuário

Os seguintes elementos de API são usados com perfis de usuário.

## <a name="functions"></a>Funções



| Função                                                                   | Descrição                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Recupera as variáveis de ambiente para o usuário especificado.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Cria um novo perfil de usuário. (Somente Windows Vista e posterior.)                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Exclui o perfil do usuário e todas as configurações relacionadas ao usuário do computador especificado.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Libera as variáveis de ambiente criadas pela função [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Expande a cadeia de caracteres de origem usando o bloco de ambiente estabelecido para o usuário especificado.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Recupera o caminho para a raiz do perfil todos os usuários.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Recupera o caminho para a raiz do perfil de usuário padrão.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Recupera o caminho para o diretório raiz onde todos os perfis de usuário são armazenados.                                  |
| [**Getprofiletype**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Recupera o tipo de perfil carregado para o usuário atual.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Recupera o caminho para o diretório raiz do perfil do usuário especificado.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Carrega o perfil do usuário especificado.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Descarrega o perfil de um usuário que foi carregado pela função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .          |



 

Não há suporte para a função [**CreateUserProfileEx**](createuserprofileex.md) .

## <a name="structures"></a>Estruturas



| Estrutura                          | Description                                |
|------------------------------------|--------------------------------------------|
| [**PROFILEINFO**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Contém informações sobre um perfil de usuário. |



 

 

 



