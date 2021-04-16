---
description: O WMI registra automaticamente a DLL do provedor de exibição durante o processo de instalação do WMI. No entanto, você ainda precisa registrar o provedor de exibição com WMI para cada namespace que conterá classes de exibição.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrando o provedor de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782455"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="6b708-104">Registrando o provedor de exibição</span><span class="sxs-lookup"><span data-stu-id="6b708-104">Registering the View Provider</span></span>

<span data-ttu-id="6b708-105">O WMI registra automaticamente a DLL do provedor de exibição durante o processo de instalação do WMI.</span><span class="sxs-lookup"><span data-stu-id="6b708-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="6b708-106">No entanto, você ainda precisa registrar o provedor de exibição com WMI para cada namespace que conterá classes de exibição.</span><span class="sxs-lookup"><span data-stu-id="6b708-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="6b708-107">O procedimento a seguir descreve como registrar o provedor de exibição.</span><span class="sxs-lookup"><span data-stu-id="6b708-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="6b708-108">**Para registrar o provedor de exibição**</span><span class="sxs-lookup"><span data-stu-id="6b708-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="6b708-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) para descrever a implementação do provedor de exibição.</span><span class="sxs-lookup"><span data-stu-id="6b708-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="6b708-110">A instância do [**\_ \_ Win32Provider**](--win32provider.md) descreve o nome do provedor e seu identificador de classe (CLSID), bem como as configurações de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="6b708-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="6b708-111">O exemplo de código a seguir descreve uma implementação do [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b708-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="6b708-112">Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="6b708-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="6b708-113">O exemplo de código a seguir mostra como criar uma instância da classe **\_ \_ InstanceProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="6b708-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="6b708-114">Crie uma instância da classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) se desejar ter os métodos de suporte da classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="6b708-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="6b708-115">O exemplo de código a seguir mostra como criar uma instância da classe **\_ \_ MethodProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="6b708-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="6b708-116">Compile seu código MOF usando o compilador MOF ([Mofcomp](mofcomp.md)) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="6b708-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="6b708-117">Se você salvar o exemplo de código MOF listado anteriormente em um arquivo chamado Viewtest. MOF, use o comando Mofcomp para carregar o código MOF no namespace de destino.</span><span class="sxs-lookup"><span data-stu-id="6b708-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="6b708-118">*NamespacePath* é o namespace no qual você deseja criar a instância da classe View.</span><span class="sxs-lookup"><span data-stu-id="6b708-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="6b708-119">Digite o seguinte comando em um prompt de comando para carregar o código MOF no namespace de destino.</span><span class="sxs-lookup"><span data-stu-id="6b708-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="6b708-120">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="6b708-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="6b708-121">Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b708-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



