---
description: Permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar Executar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controle de conta de usuário (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922451"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="a4a70-103">Controle de conta de usuário (autorização)</span><span class="sxs-lookup"><span data-stu-id="a4a70-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="a4a70-104">O UAC (controle de conta de usuário) permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar **Executar como**.</span><span class="sxs-lookup"><span data-stu-id="a4a70-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="a4a70-105">O comportamento do UAC para a configuração "nunca notificar" não desabilita mais o UAC.</span><span class="sxs-lookup"><span data-stu-id="a4a70-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="a4a70-106">A configuração "nunca notificar" fornece um token de divisão e sempre eleva automaticamente o privilégio necessário.</span><span class="sxs-lookup"><span data-stu-id="a4a70-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="a4a70-107">Essa sutileza pode fazer com que seu aplicativo tenha problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="a4a70-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="a4a70-108">Você ainda pode desabilitar o UAC usando políticas de grupo ou definindo manualmente a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="a4a70-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="a4a70-109">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** A configuração "nunca notificar" desabilita o UAC.</span><span class="sxs-lookup"><span data-stu-id="a4a70-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="a4a70-110">Por exemplo, se você executar as etapas a seguir para alterar a configuração "nunca notificar", obterá resultados diferentes ao tentar criar um arquivo em uma pasta que exija privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="a4a70-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="a4a70-111">O comportamento do Windows 8 é negar o acesso.</span><span class="sxs-lookup"><span data-stu-id="a4a70-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="a4a70-112">O comportamento do Windows 7 permite que você crie o arquivo de File.txt.</span><span class="sxs-lookup"><span data-stu-id="a4a70-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="a4a70-113">Clique ou toque em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="a4a70-113">Click or tap **Start**.</span></span> <span data-ttu-id="a4a70-114">Na caixa de pesquisa, digite "alterar configurações de controle de conta de usuário".</span><span class="sxs-lookup"><span data-stu-id="a4a70-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="a4a70-115">Clique ou toque em **alterar configurações de controle de conta de usuário** para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="a4a70-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="a4a70-116">Mova o controle deslizante para **nunca notificar**.</span><span class="sxs-lookup"><span data-stu-id="a4a70-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="a4a70-117">Clique ou toque em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4a70-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="a4a70-118">Reinicie seu computador.</span><span class="sxs-lookup"><span data-stu-id="a4a70-118">Restart your computer.</span></span>
6.  <span data-ttu-id="a4a70-119">Clique ou toque em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="a4a70-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="a4a70-120">Na caixa **abrir** , digite "Cmd.exe".</span><span class="sxs-lookup"><span data-stu-id="a4a70-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="a4a70-121">Observe que o título da janela não contém a cadeia de caracteres "administrador".</span><span class="sxs-lookup"><span data-stu-id="a4a70-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="a4a70-122">Digite "Echo >% windir% \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="a4a70-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="a4a70-123">O UAC foi adicionado no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4a70-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a4a70-124">Uma conta de usuário padrão é sinônimo de uma conta de usuário no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4a70-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="a4a70-125">As contas de usuário que são membros do grupo Administradores local executarão a maioria dos aplicativos como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="a4a70-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="a4a70-126">Para obter informações sobre o UAC, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4a70-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="a4a70-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="a4a70-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="a4a70-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4a70-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a70-129">[Diretrizes para controle de conta de usuário no desenvolvimento de IU](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="a4a70-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="a4a70-130">Informações gerais sobre o UAC.</span><span class="sxs-lookup"><span data-stu-id="a4a70-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a4a70-131">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="a4a70-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="a4a70-132">Modelos para desenvolvimento de aplicativos que executam operações que exigem privilégio administrativo, mas que são executados como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="a4a70-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="a4a70-133">Referência de autorização</span><span class="sxs-lookup"><span data-stu-id="a4a70-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="a4a70-134">Informações detalhadas sobre funções de autorização, interfaces, estruturas e outros elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="a4a70-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




