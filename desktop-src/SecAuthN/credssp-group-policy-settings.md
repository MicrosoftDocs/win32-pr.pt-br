---
description: Para o protocolo CredSSP para delegar credenciais, você deve especificar a quais servidores podem ser delegadas.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Configurações de Política de Grupo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747512"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="1824c-103">Configurações de Política de Grupo CredSSP</span><span class="sxs-lookup"><span data-stu-id="1824c-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="1824c-104">Para o [protocolo CredSSP](credential-security-support-provider.md) para delegar credenciais, você deve especificar a quais servidores podem ser delegadas.</span><span class="sxs-lookup"><span data-stu-id="1824c-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="1824c-105">Para especificar esses servidores, modifique as configurações no snap-in do GPE (console de gerenciamento Microsoft) do editor de Política de Grupo (MMC).</span><span class="sxs-lookup"><span data-stu-id="1824c-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="1824c-106">As configurações de GPE que controlam a delegação estão em **configuração do computador \| modelos administrativos \| delegação de \| credenciais do sistema**.</span><span class="sxs-lookup"><span data-stu-id="1824c-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="1824c-107">Essa não é uma delegação restrita.</span><span class="sxs-lookup"><span data-stu-id="1824c-107">This is not constrained delegation.</span></span> <span data-ttu-id="1824c-108">O CredSSP passa as credenciais completas do usuário para o servidor sem nenhuma restrição.</span><span class="sxs-lookup"><span data-stu-id="1824c-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="1824c-109">As configurações de política de grupo controlam a delegação dos seguintes tipos de credenciais.</span><span class="sxs-lookup"><span data-stu-id="1824c-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="1824c-110">Tipo de credenciais</span><span class="sxs-lookup"><span data-stu-id="1824c-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="1824c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1824c-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1824c-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciais padrão</span><span class="sxs-lookup"><span data-stu-id="1824c-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="1824c-113">As credenciais obtidas quando o usuário faz logon pela primeira vez no Windows.</span><span class="sxs-lookup"><span data-stu-id="1824c-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="1824c-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Novas credenciais</span><span class="sxs-lookup"><span data-stu-id="1824c-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="1824c-115">As credenciais para as quais o usuário é solicitado ao executar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1824c-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="1824c-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciais salvas</span><span class="sxs-lookup"><span data-stu-id="1824c-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="1824c-117">As credenciais que são salvas usando o [Gerenciador de credenciais](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="1824c-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="1824c-118">Para incluir um servidor na categoria associada a uma determinada configuração de diretiva de grupo, adicione o [*nome da entidade de serviço*](/windows/desktop/SecGloss/s-gly) (SPN) desse servidor à lista de servidores para essa configuração de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1824c-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="1824c-119">O SPN pode conter um único caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="1824c-119">The SPN can contain a single wildcard character.</span></span>

 

