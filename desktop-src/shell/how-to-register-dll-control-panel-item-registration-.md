---
description: Os itens do painel de controle que são implementados em uma DLL que exporta a função CPlApplet têm requisitos de registro diferentes dos arquivos. exe.
title: Como registrar itens do painel de controle da DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662157"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="753d3-103">Como registrar itens do painel de controle da DLL</span><span class="sxs-lookup"><span data-stu-id="753d3-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="753d3-104">As diretrizes de implementação atuais estado que os novos itens do painel de controle devem ser implementados como arquivos. exe em vez de arquivos. cpl.</span><span class="sxs-lookup"><span data-stu-id="753d3-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="753d3-105">As informações a seguir são incluídas principalmente para fins herdados.</span><span class="sxs-lookup"><span data-stu-id="753d3-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="753d3-106">Os itens do painel de controle que são implementados em uma DLL que exporta a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) têm requisitos de registro diferentes dos arquivos. exe.</span><span class="sxs-lookup"><span data-stu-id="753d3-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="753d3-107">A partir do Windows XP, novas DLLs de item do painel de controle devem ser instaladas na pasta do aplicativo associado na pasta arquivos de programas.</span><span class="sxs-lookup"><span data-stu-id="753d3-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="753d3-108">Os itens que são armazenados no diretório system32 com uma extensão. cpl não precisam ser registrados; Eles são mostrados automaticamente no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="753d3-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="753d3-109">Todos os outros itens do painel de controle que usam **CPlApplet** devem ser registrados de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="753d3-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="753d3-110">Se o item do painel de controle estiver disponível para todos os usuários, registre o caminho por computador adicionando um valor **reg \_ expande \_ sz** à subchave **HKEY \_ \_ local** Computer \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** \\ **CPLs** , definida como o caminho da dll.</span><span class="sxs-lookup"><span data-stu-id="753d3-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="753d3-111">Se o item do painel de controle estiver disponível em uma base por usuário, use **HKEY \_ Current \_ User** como a chave raiz em vez de **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="753d3-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="753d3-112">Os dois exemplos a seguir registram o item do painel de controle do *MyCplApp* .</span><span class="sxs-lookup"><span data-stu-id="753d3-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="753d3-113">A DLL é denominada MyCpl.cpl e está localizada no diretório de aplicativo *MyCorp \\ MyApp* .</span><span class="sxs-lookup"><span data-stu-id="753d3-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="753d3-114">Este primeiro exemplo ilustra o registro por computador.</span><span class="sxs-lookup"><span data-stu-id="753d3-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="753d3-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="753d3-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="753d3-116">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="753d3-116">Step 1:</span></span>

<span data-ttu-id="753d3-117">Adicione essas informações ao registro para registrar a existência do arquivo. cpl.</span><span class="sxs-lookup"><span data-stu-id="753d3-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="753d3-118">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="753d3-118">Step 2:</span></span>

<span data-ttu-id="753d3-119">**Windows Vista e posterior:** Adicione essas informações adicionais ao registro para fornecer um GUID para o item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="753d3-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="753d3-120">Ao gerar um GUID para identificar exclusivamente o item do painel de controle, você pode adicionar links de tarefas ao painel de controle.</span><span class="sxs-lookup"><span data-stu-id="753d3-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="753d3-121">Sem esse GUID, não há nenhuma maneira de os links de tarefa serem associados ao item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="753d3-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="753d3-122">Consulte [criando links de tarefas pesquisáveis para obter um item do painel de controle](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="753d3-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="753d3-123">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="753d3-123">Step 3:</span></span>

<span data-ttu-id="753d3-124">**Windows Vista e posterior:** Adicione as seguintes informações ao registro para criar um nome canônico para o item.</span><span class="sxs-lookup"><span data-stu-id="753d3-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="753d3-125">Ao adicionar um nome canônico, os usuários podem iniciar o item do painel de controle em uma linha de comando digitando `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="753d3-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="753d3-126">Isso também torna possível alterar uma implementação de um arquivo. cpl para um arquivo. exe mais tarde, sem a necessidade de chamar programas para fazer alterações, já que eles podem continuar abrindo o item por meio de seu nome canônico.</span><span class="sxs-lookup"><span data-stu-id="753d3-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="753d3-127">Para obter mais informações sobre nomes canônicos, consulte [executando itens do painel de controle](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="753d3-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="753d3-128">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="753d3-128">Step 4:</span></span>

<span data-ttu-id="753d3-129">**Windows Vista e posterior:** Adicione as seguintes informações ao registro para atribuir um item do painel de controle a uma ou mais categorias.</span><span class="sxs-lookup"><span data-stu-id="753d3-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="753d3-130">**Windows XP:** Adicione as seguintes informações ao registro para atribuir um item do painel de controle a uma ou mais categorias.</span><span class="sxs-lookup"><span data-stu-id="753d3-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="753d3-131">Este exemplo atribui o item à categoria 3, que é rede e Internet.</span><span class="sxs-lookup"><span data-stu-id="753d3-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="753d3-132">Para adicionar um item a várias categorias, forneça a lista como um valor de sz de REG \_ separado por vírgulas, como "3, 8".</span><span class="sxs-lookup"><span data-stu-id="753d3-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="753d3-133">Os valores podem ser fornecidos como Decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="753d3-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="753d3-134">Observe que a capacidade de adicionar um item a várias categorias só é possível no Windows XP Service Pack 2 (SP2) e posterior.</span><span class="sxs-lookup"><span data-stu-id="753d3-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="753d3-135">Consulte [atribuindo categorias do painel de controle](assigning-control-panel-categories.md) para todos os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="753d3-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="753d3-136">Etapa 5:</span><span class="sxs-lookup"><span data-stu-id="753d3-136">Step 5:</span></span>

<span data-ttu-id="753d3-137">**Windows Vista e posterior:** Adicione as seguintes informações ao registro para criar e apontar para um arquivo XML para manter os links de tarefas para o item.</span><span class="sxs-lookup"><span data-stu-id="753d3-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="753d3-138">O valor deve ser um \_ caminho reg sz, como mostrado aqui ou um módulo e uma ID de recurso (por exemplo, "C: \\ Program Files \\ mycorp \\ MyApp \\MyApp.exe,-31") se for um recurso incorporado.</span><span class="sxs-lookup"><span data-stu-id="753d3-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="753d3-139">O local do arquivo XML deve ser totalmente especificado.</span><span class="sxs-lookup"><span data-stu-id="753d3-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="753d3-140">Ele não pode usar uma variável de ambiente, como% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="753d3-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="753d3-141">Para obter mais detalhes sobre links de tarefas e como criar o arquivo XML para contê-los, consulte [criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="753d3-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="753d3-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="753d3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="753d3-143">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="753d3-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="753d3-144">Como registrar itens do painel de controle executável</span><span class="sxs-lookup"><span data-stu-id="753d3-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
