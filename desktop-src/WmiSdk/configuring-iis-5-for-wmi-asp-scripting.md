---
description: Todas as configurações de autenticação são feitas por meio do Gerenciador de Serviços de Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configurando o IIS 5,0 e posterior para o script WMI ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788755"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="cf363-103">Configurando o IIS 5,0 e posterior para o script WMI ASP</span><span class="sxs-lookup"><span data-stu-id="cf363-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="cf363-104">Todas as configurações de autenticação são feitas por meio do Gerenciador de Serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="cf363-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="cf363-105">Ao configurar o IIS (servidor de informações da Internet) 5,0 e a segurança do IIS 6,0 para scripts ASP WMI, considere os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cf363-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="cf363-106">Nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="cf363-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="cf363-107">Você pode configurar no nível do servidor, diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="cf363-108">Configuração de autenticação</span><span class="sxs-lookup"><span data-stu-id="cf363-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="cf363-109">Você pode definir a autenticação para o Windows anônimo, integrado ou ambos.</span><span class="sxs-lookup"><span data-stu-id="cf363-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="cf363-110">Proteção</span><span class="sxs-lookup"><span data-stu-id="cf363-110">Protection</span></span>](#protection)

    <span data-ttu-id="cf363-111">Você pode definir o ASP para executar em processo (baixa proteção) ou fora do processo usando Dllhost.exe (proteção média ou alta).</span><span class="sxs-lookup"><span data-stu-id="cf363-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="cf363-112">Nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="cf363-112">Authentication Level</span></span>

<span data-ttu-id="cf363-113">Para aumentar a segurança, você pode configurar a autenticação no nível do diretório ou do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="cf363-114">Se a autenticação estiver definida no nível do servidor, todos os diretórios e arquivos subsequentes aderirão à autenticação do servidor, a menos que sejam explicitamente alterados no nível do diretório ou do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="cf363-115">Você pode criar uma estrutura de diretório para conter todos os scripts WMI ASP em que as páginas HTML e ASPs específicas ao WMI podem ser configuradas independentemente do restante do servidor.</span><span class="sxs-lookup"><span data-stu-id="cf363-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="cf363-116">Execute o procedimento a seguir para alterar o nível de autenticação de um servidor, diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="cf363-117">**Para definir a autenticação em qualquer nível**</span><span class="sxs-lookup"><span data-stu-id="cf363-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="cf363-118">No painel de controle, clique duas vezes em **Ferramentas administrativas** e, em seguida, clique duas vezes no snap-in do IIS.</span><span class="sxs-lookup"><span data-stu-id="cf363-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="cf363-119">Localize o ícone da página ASP e, em seguida, abra as propriedades do nível a ser definido, que pode ser servidor, diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="cf363-120">Configurações de autenticação estão localizadas na guia Segurança de **diretório** ou **segurança de arquivo** da folha de **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="cf363-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="cf363-121">Configuração de autenticação</span><span class="sxs-lookup"><span data-stu-id="cf363-121">Authentication Setting</span></span>

<span data-ttu-id="cf363-122">Para scripts ASP WMI, a combinação de autenticação anônima desativada (desmarcada) e a autenticação integrada do Windows ativada (marcada) fornece uma oportunidade maior para definir a segurança.</span><span class="sxs-lookup"><span data-stu-id="cf363-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="cf363-123">Para usar as configurações de autenticação do NT LAN Manager (NTLM), Passport ou Digest do IIS, você deve ativar os privilégios de habilitação remota, pois o usuário é tratado como uma identidade de rede e registrado remotamente.</span><span class="sxs-lookup"><span data-stu-id="cf363-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="cf363-124">A configuração habilitação remota não é necessária para a autenticação anônima e básica.</span><span class="sxs-lookup"><span data-stu-id="cf363-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="cf363-125">No entanto, o sistema é muito menos seguro quando você está usando a autenticação anônima e básica.</span><span class="sxs-lookup"><span data-stu-id="cf363-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="cf363-126">Se a autenticação anônima for usada com ou sem a autenticação integrada do Windows, a abordagem mais segura será usar um logon que exija que um usuário insira um nome de usuários e uma senha.</span><span class="sxs-lookup"><span data-stu-id="cf363-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="cf363-127">O logon padrão é a identidade do IIS, mas um logon pode ser criado usando permissões específicas adequadas para os scripts ASP WMI que podem ser usados como a conta para as conexões anônimas ou convidadas.</span><span class="sxs-lookup"><span data-stu-id="cf363-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="cf363-128">Se você escolher um identificador de logon que não seja uma identidade do IIS, desmarque a caixa de seleção **permitir que o IIS controle a senha** e insira a senha correta.</span><span class="sxs-lookup"><span data-stu-id="cf363-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="cf363-129">Isso força todas as conexões anônimas ou convidadas a usar o identificador de logon.</span><span class="sxs-lookup"><span data-stu-id="cf363-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="cf363-130">Ao criar um logon separado da identidade do IIS, os privilégios de uma conta que acessa o WMI podem ser controlados sem afetar os outros diretórios ou arquivos no servidor IIS, a menos que a autenticação esteja definida no nível do servidor.</span><span class="sxs-lookup"><span data-stu-id="cf363-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="cf363-131">Execute o procedimento a seguir para definir os requisitos de autenticação para a página ASP usando o snap-in do IIS no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="cf363-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="cf363-132">**Para acessar a configuração da conta**</span><span class="sxs-lookup"><span data-stu-id="cf363-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="cf363-133">No painel de controle, clique duas vezes no ícone **Ferramentas administrativas** , abra o snap-in do IIS, localize a página ASP e abra as propriedades do nível a ser definido, que pode ser servidor, diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf363-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="cf363-134">As configurações de autenticação podem ser encontradas na guia Segurança de **diretório** ou **segurança de arquivo** da folha **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="cf363-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="cf363-135">Na área autenticação anônima, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="cf363-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="cf363-136">Se um identificador de logon diferente da identidade do IIS for selecionado, desmarque a caixa de seleção **permitir que o IIS controle a senha** e insira a senha correta.</span><span class="sxs-lookup"><span data-stu-id="cf363-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="cf363-137">Isso força todas as conexões anônimas ou convidadas a usar o identificador de logon.</span><span class="sxs-lookup"><span data-stu-id="cf363-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="cf363-138">Usando um logon diferente da identidade do IIS, os privilégios da conta que acessa o WMI podem ser controlados sem afetar os outros diretórios ou arquivos no servidor IIS, a menos que a autenticação esteja definida no nível do servidor.</span><span class="sxs-lookup"><span data-stu-id="cf363-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="cf363-139">A configuração anterior permite que o servidor IIS use a autenticação anônima em algumas áreas e uma autenticação integrada do Windows ou mista em outras.</span><span class="sxs-lookup"><span data-stu-id="cf363-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="cf363-140">Proteção</span><span class="sxs-lookup"><span data-stu-id="cf363-140">Protection</span></span>

<span data-ttu-id="cf363-141">A última consideração ao configurar o servidor IIS é a proteção a ser usada ao executar um ASP.</span><span class="sxs-lookup"><span data-stu-id="cf363-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="cf363-142">Você pode definir um ASP para executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cf363-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="cf363-143">Em processo para o IIS (baixa proteção).</span><span class="sxs-lookup"><span data-stu-id="cf363-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="cf363-144">Externo ao IIS com Dllhost.exe como em pool ou fora de processo (proteção de mídia em pool).</span><span class="sxs-lookup"><span data-stu-id="cf363-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="cf363-145">Auto-host fora do processo (alta proteção).</span><span class="sxs-lookup"><span data-stu-id="cf363-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="cf363-146">Para obter o melhor equilíbrio de segurança e desempenho, use o host em pool.</span><span class="sxs-lookup"><span data-stu-id="cf363-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



