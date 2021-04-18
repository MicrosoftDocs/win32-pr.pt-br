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
# <a name="mandatory-user-profiles"></a><span data-ttu-id="e2089-103">Perfis de usuário obrigatórios</span><span class="sxs-lookup"><span data-stu-id="e2089-103">Mandatory User Profiles</span></span>

<span data-ttu-id="e2089-104">Um perfil de usuário obrigatório é um tipo especial de perfil de [usuário de roaming](roaming-user-profiles.md) pré-configurado que os administradores podem usar para especificar as configurações para os usuários.</span><span class="sxs-lookup"><span data-stu-id="e2089-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="e2089-105">Com perfis de usuário obrigatórios, um usuário pode modificar sua área de trabalho, mas as alterações não são salvas quando o usuário faz logoff.</span><span class="sxs-lookup"><span data-stu-id="e2089-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="e2089-106">Na próxima vez que o usuário fizer logon, o perfil de usuário obrigatório criado pelo administrador será baixado.</span><span class="sxs-lookup"><span data-stu-id="e2089-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="e2089-107">Há dois tipos de perfis obrigatórios: perfis *obrigatórios normais* e perfis *super obrigatórios* .</span><span class="sxs-lookup"><span data-stu-id="e2089-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="e2089-108">Os perfis de usuário se tornam perfis obrigatórios quando o administrador renomeia o arquivo NTuser. dat (o hive do registro) no servidor para NTuser. Man.</span><span class="sxs-lookup"><span data-stu-id="e2089-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="e2089-109">A extensão. Man faz com que o perfil do usuário seja um perfil somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e2089-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="e2089-110">Os perfis de usuário se tornam *extremamente obrigatórios* quando o nome da pasta do caminho do perfil termina em. Man; por exemplo, \\ \\ Server \\ share \\ mandatoryprofile. Man \\ .</span><span class="sxs-lookup"><span data-stu-id="e2089-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="e2089-111">Os perfis de usuário superobrigatórios são semelhantes aos perfis obrigatórios normais, com exceção de que os usuários que têm perfis superobrigatórios não podem fazer logon quando o servidor que armazena o perfil obrigatório está indisponível.</span><span class="sxs-lookup"><span data-stu-id="e2089-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="e2089-112">Os usuários com perfis obrigatórios normais podem fazer logon com a cópia armazenada em cache localmente do perfil obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e2089-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="e2089-113">Somente administradores do sistema podem fazer alterações em perfis de usuário obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e2089-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



