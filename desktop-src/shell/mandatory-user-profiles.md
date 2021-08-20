---
description: Um perfil de usuário obrigatório é um tipo especial de perfil de usuário em roaming pré-configurado que os administradores podem usar para especificar configurações para usuários.
title: Perfis de Usuário Obrigatórios
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 748135affd0b6be399242ff171c88a45da3047911f0603f47eccf0a1f0ba0018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678140"
---
# <a name="mandatory-user-profiles"></a>Perfis de Usuário Obrigatórios

Um perfil de usuário obrigatório é um tipo especial de perfil de usuário [em roaming](roaming-user-profiles.md) pré-configurado que os administradores podem usar para especificar configurações para usuários. Com perfis de usuário obrigatórios, um usuário pode modificar sua área de trabalho, mas as alterações não são salvas quando o usuário faz o login. Na próxima vez que o usuário faz logo depois, o perfil de usuário obrigatório criado pelo administrador é baixado. Há dois tipos de perfis obrigatórios: *perfis obrigatórios normais* e *perfis super obrigatórios.*

Os perfis de usuário se tornam perfis obrigatórios quando o administrador renomeia o arquivo NTuser.dat (o hive do Registro) no servidor para NTuser.man. A extensão .man faz com que o perfil do usuário seja um perfil somente leitura.

Os perfis de usuário *se tornam super obrigatórios* quando o nome da pasta do caminho do perfil termina em .man; por exemplo, \\ \\ \\ compartilhamento de \\ servidor mandatoryprofile.man. \\

Perfis de usuário super obrigatórios são semelhantes aos perfis obrigatórios normais, com exceção de que os usuários que têm perfis super obrigatórios não podem fazer logoff quando o servidor que armazena o perfil obrigatório não está disponível. Os usuários com perfis obrigatórios normais podem fazer logoff com a cópia armazenada em cache localmente do perfil obrigatório.

Somente os administradores do sistema podem fazer alterações em perfis de usuário obrigatórios.

 

 



