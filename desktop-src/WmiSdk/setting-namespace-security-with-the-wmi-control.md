---
description: O controle WMI é um snap-in do MMC localizado no painel de controle e é usado para definir manualmente a segurança do namespace do WMI em um computador local. Você também pode definir o namespace padrão para scripts.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Definindo a segurança do namespace com o controle WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807906"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="54869-104">Definindo a segurança do namespace com o controle WMI</span><span class="sxs-lookup"><span data-stu-id="54869-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="54869-105">O controle WMI é um snap-in do MMC localizado no **painel de controle** e é usado para definir manualmente a segurança do namespace do WMI em um computador local.</span><span class="sxs-lookup"><span data-stu-id="54869-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="54869-106">Você também pode definir o namespace padrão para scripts.</span><span class="sxs-lookup"><span data-stu-id="54869-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="54869-107">O procedimento a seguir descreve como localizar o controle WMI.</span><span class="sxs-lookup"><span data-stu-id="54869-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="54869-108">**Para localizar o controle WMI**</span><span class="sxs-lookup"><span data-stu-id="54869-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="54869-109">No **painel de controle**, clique duas vezes em **Ferramentas administrativas**.</span><span class="sxs-lookup"><span data-stu-id="54869-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="54869-110">Na janela **Ferramentas Administrativas**, clique duas vezes em **Gerenciamento de Computador**.</span><span class="sxs-lookup"><span data-stu-id="54869-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="54869-111">Na janela **Gerenciamento do computador** , expanda a árvore **serviços e aplicativos** e clique duas vezes no **controle WMI**.</span><span class="sxs-lookup"><span data-stu-id="54869-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="54869-112">Clique com o botão direito do mouse no ícone **controle WMI** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="54869-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="54869-113">O procedimento a seguir descreve como usar o controle WMI para configurar a segurança de um namespace como um modelo e, em seguida, obter as configurações de segurança programaticamente para definir a segurança para outros namespaces.</span><span class="sxs-lookup"><span data-stu-id="54869-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="54869-114">**Para definir a segurança do namespace com o controle WMI**</span><span class="sxs-lookup"><span data-stu-id="54869-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="54869-115">Crie um novo namespace usando o código formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="54869-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="54869-116">Execute o controle WMI para definir a segurança no novo namespace.</span><span class="sxs-lookup"><span data-stu-id="54869-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="54869-117">No menu **Iniciar** , clique em **executar** e digite **wmimgmt. msc** ou consulte [localizando o controle WMI](#).</span><span class="sxs-lookup"><span data-stu-id="54869-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="54869-118">No painel **controle WMI** , clique com o botão direito do mouse em **controle WMI**, escolha **Propriedades** e, em seguida, selecione a guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="54869-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="54869-119">Navegue até o novo namespace, clique em **segurança** e, em seguida, configure grupos e permissões para o namespace.</span><span class="sxs-lookup"><span data-stu-id="54869-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="54869-120">Você também pode usar Instrumentação de Gerenciamento do Windows Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) para definir a segurança do namespace.</span><span class="sxs-lookup"><span data-stu-id="54869-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="54869-121">Para obter mais informações, consulte [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="54869-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="54869-122">Definindo o namespace padrão para scripts</span><span class="sxs-lookup"><span data-stu-id="54869-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="54869-123">Se um script não se conectar explicitamente a um namespace ao se conectar ao WMI, o WMI usará o namespace padrão especificado nesse controle.</span><span class="sxs-lookup"><span data-stu-id="54869-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="54869-124">O padrão também é encontrado na entrada do registro da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="54869-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="54869-125">Como o namespace padrão é fácil de alterar, com esse controle ou programaticamente chamando métodos de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), especifique o namespace ao se conectar ao WMI por meio do [moniker](constructing-a-moniker-string.md) ou chamadas para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="54869-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="54869-126">Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md)</span><span class="sxs-lookup"><span data-stu-id="54869-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="54869-127">**Para definir o namespace padrão para scripts**</span><span class="sxs-lookup"><span data-stu-id="54869-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="54869-128">Na janela **Propriedades do controle WMI** , escolha a guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="54869-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="54869-129">Clique no botão **alterar** e selecione o namespace para tornar o padrão.</span><span class="sxs-lookup"><span data-stu-id="54869-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54869-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54869-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54869-131">Definindo descritores de segurança de namespace</span><span class="sxs-lookup"><span data-stu-id="54869-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
