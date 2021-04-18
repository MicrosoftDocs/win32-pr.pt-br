---
description: Um perfil de usuário obrigatório é um tipo especial de perfil de usuário de roaming pré-configurado que os administradores podem usar para especificar as configurações para os usuários.
title: Perfis de usuário obrigatórios
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501143"
---
# <a name="mandatory-user-profiles"></a>Perfis de usuário obrigatórios

Um perfil de usuário obrigatório é um tipo especial de perfil de [usuário de roaming](roaming-user-profiles.md) pré-configurado que os administradores podem usar para especificar as configurações para os usuários. Com perfis de usuário obrigatórios, um usuário pode modificar sua área de trabalho, mas as alterações não são salvas quando o usuário faz logoff. Na próxima vez que o usuário fizer logon, o perfil de usuário obrigatório criado pelo administrador será baixado. Há dois tipos de perfis obrigatórios: perfis *obrigatórios normais* e perfis *super obrigatórios* .

Os perfis de usuário se tornam perfis obrigatórios quando o administrador renomeia o arquivo NTuser. dat (o hive do registro) no servidor para NTuser. Man. A extensão. Man faz com que o perfil do usuário seja um perfil somente leitura.

Os perfis de usuário se tornam *extremamente obrigatórios* quando o nome da pasta do caminho do perfil termina em. Man; por exemplo, \\ \\ Server \\ share \\ mandatoryprofile. Man \\ .

Os perfis de usuário superobrigatórios são semelhantes aos perfis obrigatórios normais, com exceção de que os usuários que têm perfis superobrigatórios não podem fazer logon quando o servidor que armazena o perfil obrigatório está indisponível. Os usuários com perfis obrigatórios normais podem fazer logon com a cópia armazenada em cache localmente do perfil obrigatório.

Somente administradores do sistema podem fazer alterações em perfis de usuário obrigatórios.

 

 



