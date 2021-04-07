---
description: A DLL de filtro de senha do Windows, Passfilt.dll, é executada no contexto de segurança da conta do sistema local e ajuda você a filtrar senhas de conta local ou de domínio.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalando e registrando uma DLL de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828552"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="2245d-103">Instalando e registrando uma DLL de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2245d-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="2245d-104">Você pode usar o filtro de senha do Windows para filtrar as senhas de conta local ou de domínio.</span><span class="sxs-lookup"><span data-stu-id="2245d-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="2245d-105">Para usar o filtro de senha para contas de domínio, instale e registre a DLL em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="2245d-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="2245d-106">Execute as etapas a seguir para instalar o filtro de senha.</span><span class="sxs-lookup"><span data-stu-id="2245d-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="2245d-107">Você pode executar essas etapas manualmente ou pode escrever um instalador para executar essas etapas.</span><span class="sxs-lookup"><span data-stu-id="2245d-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="2245d-108">Você precisa ser um administrador ou pertencer ao grupo de administradores para executar essas etapas.</span><span class="sxs-lookup"><span data-stu-id="2245d-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="2245d-109">**Para instalar e registrar uma DLL de filtro de senha do Windows**</span><span class="sxs-lookup"><span data-stu-id="2245d-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="2245d-110">Copie a DLL para o diretório de instalação do Windows no controlador de domínio ou no computador local.</span><span class="sxs-lookup"><span data-stu-id="2245d-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="2245d-111">Em instalações padrão, a pasta padrão é \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="2245d-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="2245d-112">Certifique-se de criar uma DLL de filtro de senha de 32 bits para computadores de 32 bits e uma DLL de filtro de senha de 64 bits para computadores de 64 bits e, em seguida, copie-os para o local apropriado.</span><span class="sxs-lookup"><span data-stu-id="2245d-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="2245d-113">Para registrar o filtro de senha, atualize a seguinte chave do registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="2245d-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="2245d-114">Se a subchave **pacotes de notificação** existir, adicione o nome da sua dll aos dados do valor existente.</span><span class="sxs-lookup"><span data-stu-id="2245d-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="2245d-115">Não substitua os valores existentes e não inclua a extensão. dll.</span><span class="sxs-lookup"><span data-stu-id="2245d-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="2245d-116">Se a subchave **pacotes de notificação** não existir, adicione-a e, em seguida, especifique o nome da dll para os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="2245d-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="2245d-117">Não inclua a extensão. dll.</span><span class="sxs-lookup"><span data-stu-id="2245d-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="2245d-118">A subchave **pacotes de notificação** pode adicionar vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="2245d-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="2245d-119">Localize a configuração de complexidade da senha.</span><span class="sxs-lookup"><span data-stu-id="2245d-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="2245d-120">No painel de controle, clique em **desempenho e manutenção**, clique em **Ferramentas administrativas**, clique duas vezes em **política de segurança local**, clique duas vezes em **políticas de conta** e clique duas vezes em **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="2245d-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="2245d-121">Para impor o filtro de senha padrão do Windows e o filtro de senha personalizada, verifique se a configuração de política **senhas devem atender aos requisitos de complexidade** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2245d-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="2245d-122">Caso contrário, desabilite a configuração de política as **senhas devem atender aos requisitos de complexidade** .</span><span class="sxs-lookup"><span data-stu-id="2245d-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2245d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2245d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2245d-124">Considerações sobre programação de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2245d-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="2245d-125">Imposição de senha forte e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="2245d-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="2245d-126">Funções de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2245d-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



