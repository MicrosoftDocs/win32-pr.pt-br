---
description: Substituições do administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Substituições do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758927"
---
# <a name="administrator-overrides"></a><span data-ttu-id="c0a9b-103">Substituições do administrador</span><span class="sxs-lookup"><span data-stu-id="c0a9b-103">Administrator Overrides</span></span>

<span data-ttu-id="c0a9b-104">O Windows tem uma única ACL (lista de controle de acesso) padrão em todos os objetos de política de energia.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="c0a9b-105">A ACL concede permissões de leitura, gravação e alteração aos membros do grupo de usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="c0a9b-106">Todos os outros usuários recebem permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="c0a9b-107">Aplicativos que chamam funções de política de energia podem determinar se um usuário tem permissões para uma configuração de energia especificada usando a função [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="c0a9b-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="c0a9b-108">As configurações de energia podem ser substituídas por meio de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="c0a9b-109">As substituições podem ser definidas por meio da política de grupo de domínio ou da política de grupo local.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="c0a9b-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) relatará se uma configuração de energia especificada tiver uma substituição de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="c0a9b-111">A ferramenta de linha de comando **PowerCfg.exe** exibe uma mensagem de erro quando um comando não pode ser concluído porque o usuário não tinha permissões para alterar a configuração de energia ou porque a configuração de energia tem uma substituição de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="c0a9b-112">O aplicativo opções de energia no painel de controle não fornece suporte para configurar permissões de acesso à política de energia.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="c0a9b-113">A alteração de permissões deve ser feita via **PowerCfg.exe**.</span><span class="sxs-lookup"><span data-stu-id="c0a9b-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



