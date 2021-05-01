---
description: A DLL de filtro de senha do Windows, Passfilt.dll, é executada no contexto de segurança da conta do sistema local e ajuda você a filtrar senhas de conta local ou de domínio.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalando e registrando uma DLL de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327161"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="2a70a-103">Instalando e registrando uma DLL de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2a70a-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="2a70a-104">Você pode usar o filtro de senha do Windows para filtrar as senhas de conta local ou de domínio.</span><span class="sxs-lookup"><span data-stu-id="2a70a-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="2a70a-105">Para usar o filtro de senha para contas de domínio, instale e registre a DLL em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="2a70a-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="2a70a-106">Execute as etapas a seguir para instalar o filtro de senha.</span><span class="sxs-lookup"><span data-stu-id="2a70a-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="2a70a-107">Você pode executar essas etapas manualmente ou pode escrever um instalador para executar essas etapas.</span><span class="sxs-lookup"><span data-stu-id="2a70a-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="2a70a-108">Você precisa ser um administrador ou pertencer ao grupo de administradores para executar essas etapas.</span><span class="sxs-lookup"><span data-stu-id="2a70a-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="2a70a-109">**Para instalar e registrar uma DLL de filtro de senha do Windows**</span><span class="sxs-lookup"><span data-stu-id="2a70a-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="2a70a-110">Copie a DLL para o diretório de instalação do Windows no controlador de domínio ou no computador local.</span><span class="sxs-lookup"><span data-stu-id="2a70a-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="2a70a-111">Em instalações padrão, a pasta padrão é \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="2a70a-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="2a70a-112">Certifique-se de criar uma DLL de filtro de senha de 32 bits para computadores de 32 bits e uma DLL de filtro de senha de 64 bits para computadores de 64 bits e, em seguida, copie-os para o local apropriado.</span><span class="sxs-lookup"><span data-stu-id="2a70a-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="2a70a-113">Para registrar o filtro de senha, atualize a seguinte chave do registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="2a70a-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="2a70a-114">Se o valor dos **pacotes de notificação** do tipo *REG_MULTI_SZ* existir, adicione o nome da sua dll aos dados do valor existente.</span><span class="sxs-lookup"><span data-stu-id="2a70a-114">If the **Notification Packages** value of type *REG_MULTI_SZ* exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="2a70a-115">Não substitua os valores existentes e não inclua a extensão. dll.</span><span class="sxs-lookup"><span data-stu-id="2a70a-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="2a70a-116">Se o valor dos **pacotes de notificação** não existir, crie-o, dê a ele o tipo de *REG_MULTI_SZ* e, em seguida, ESPECIFIQUE o nome da dll para os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="2a70a-116">If the **Notification Packages** value does not exist, create it, give it the *REG_MULTI_SZ* type and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="2a70a-117">Não inclua a extensão. dll.</span><span class="sxs-lookup"><span data-stu-id="2a70a-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="2a70a-118">O valor dos **pacotes de notificação** pode adicionar vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="2a70a-118">The **Notification Packages** value can add multiple packages.</span></span>

3.  <span data-ttu-id="2a70a-119">Localize a configuração de complexidade da senha.</span><span class="sxs-lookup"><span data-stu-id="2a70a-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="2a70a-120">No painel de controle, clique em **desempenho e manutenção**, clique em **Ferramentas administrativas**, clique duas vezes em **política de segurança local**, clique duas vezes em **políticas de conta** e clique duas vezes em **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="2a70a-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="2a70a-121">Para impor o filtro de senha padrão do Windows e o filtro de senha personalizada, verifique se a configuração de política **senhas devem atender aos requisitos de complexidade** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2a70a-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="2a70a-122">Caso contrário, desabilite a configuração de política as **senhas devem atender aos requisitos de complexidade** .</span><span class="sxs-lookup"><span data-stu-id="2a70a-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a70a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a70a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a70a-124">Considerações sobre programação de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2a70a-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="2a70a-125">Imposição de senha forte e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="2a70a-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="2a70a-126">Funções de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="2a70a-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



