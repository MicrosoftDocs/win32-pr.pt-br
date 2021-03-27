---
description: Para itens do painel de controle que são implementados como arquivos. exe, nenhuma exportação especial ou manipulação de mensagens é necessária. Qualquer arquivo. exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta do painel de controle.
title: Como registrar itens do painel de controle executável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011004"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="6eec1-104">Como registrar itens do painel de controle executável</span><span class="sxs-lookup"><span data-stu-id="6eec1-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="6eec1-105">Para itens do painel de controle que são implementados como arquivos. exe, nenhuma exportação especial ou manipulação de mensagens é necessária.</span><span class="sxs-lookup"><span data-stu-id="6eec1-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="6eec1-106">Qualquer arquivo. exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="6eec1-107">Um exemplo é usado aqui para demonstrar os requisitos de registro.</span><span class="sxs-lookup"><span data-stu-id="6eec1-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="6eec1-108">O exemplo mostra como registrar um item do painel de controle chamado **minhas configurações** como um objeto de comando para que ele apareça na janela do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="6eec1-109">A janela **minhas configurações** também aparece quando o comando `MyApp.exe /settings` é executado.</span><span class="sxs-lookup"><span data-stu-id="6eec1-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="6eec1-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="6eec1-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6eec1-111">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="6eec1-111">Step 1:</span></span>

<span data-ttu-id="6eec1-112">Gere um GUID para o item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="6eec1-113">O GUID identifica exclusivamente o item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="6eec1-114">Neste exemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` é o GUID do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="6eec1-115">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="6eec1-115">Step 2:</span></span>

<span data-ttu-id="6eec1-116">Usando o GUID como um nome, adicione uma subchave ao registro da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6eec1-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="6eec1-117">Os dados para a entrada padrão são simplesmente o \_ nome do reg sz do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="6eec1-118">A entrada padrão pode ser útil para identificar a entrada GUID, mas é opcional.</span><span class="sxs-lookup"><span data-stu-id="6eec1-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="6eec1-119">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="6eec1-119">Step 3:</span></span>

<span data-ttu-id="6eec1-120">Usando o GUID como um nome, adicione uma subchave e suas entradas ao registro da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6eec1-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="6eec1-121">**Default**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-121">**Default**.</span></span> <span data-ttu-id="6eec1-122">REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-122">REG\_SZ.</span></span> <span data-ttu-id="6eec1-123">O nome de exibição do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="6eec1-124">**Localizadastring**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-124">**LocalizedString**.</span></span> <span data-ttu-id="6eec1-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6eec1-125">Optional.</span></span> <span data-ttu-id="6eec1-126">REG \_ sz ou reg \_ expande \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="6eec1-127">O nome do módulo e a ID da tabela de cadeia de caracteres do nome localizado do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="6eec1-128">O formato é um sinal de "arroba" (@) seguido pelo nome do. exe ou. dll que contém a tabela de cadeia de caracteres MUI (Multilingual User interface).</span><span class="sxs-lookup"><span data-stu-id="6eec1-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="6eec1-129">As variáveis de ambiente podem ser usadas como um substituto para uma parte do caminho.</span><span class="sxs-lookup"><span data-stu-id="6eec1-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="6eec1-130">O caminho e o nome do arquivo são seguidos por uma vírgula (,) e um hífen (-), seguidos da ID na tabela de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6eec1-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="6eec1-131">Se o módulo não tiver uma tabela de cadeia de caracteres, essa entrada poderá simplesmente ser a cadeia de caracteres do nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="6eec1-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="6eec1-132">Se você usar apenas a cadeia de caracteres de nome de exibição em vez de uma tabela de cadeia de caracteres, o nome não será ajustado para o idioma de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="6eec1-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="6eec1-133">**InfoTip**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-133">**InfoTip**.</span></span> <span data-ttu-id="6eec1-134">REG \_ sz ou reg \_ expande \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="6eec1-135">Uma descrição do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-135">A description of the Control Panel item.</span></span> <span data-ttu-id="6eec1-136">Essas informações são mostradas em um InfoTip que é exibido quando o mouse passa sobre o ícone do item.</span><span class="sxs-lookup"><span data-stu-id="6eec1-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="6eec1-137">A sintaxe é a mesma usada para a Localizadastring, incluindo a opção de simplesmente fornecer uma cadeia de caracteres em vez de uma referência de tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6eec1-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="6eec1-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-138">**System.ApplicationName**.</span></span> <span data-ttu-id="6eec1-139">REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-139">REG\_SZ.</span></span> <span data-ttu-id="6eec1-140">O nome canônico do item.</span><span class="sxs-lookup"><span data-stu-id="6eec1-140">The canonical name of the item.</span></span> <span data-ttu-id="6eec1-141">O comando do formulário `control.exe /name System.ApplicationName` abre o item; por exemplo, `control.exe /name MyCorporation.MySettings` .</span><span class="sxs-lookup"><span data-stu-id="6eec1-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="6eec1-142">Consulte [executando itens do painel de controle](executing-control-panel-items.md) para obter mais informações sobre o uso de Control.exe.</span><span class="sxs-lookup"><span data-stu-id="6eec1-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="6eec1-143">**System. ControlPanel. Category**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="6eec1-144">REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-144">REG\_SZ.</span></span> <span data-ttu-id="6eec1-145">Um valor que declara as categorias do painel de controle em que o item é exibido.</span><span class="sxs-lookup"><span data-stu-id="6eec1-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="6eec1-146">Várias categorias são separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6eec1-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="6eec1-147">No caso do exemplo acima, a entrada especifica que o item **minhas configurações** deve aparecer nas categorias **aparência e personalização** e **programas** .</span><span class="sxs-lookup"><span data-stu-id="6eec1-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="6eec1-148">Consulte [atribuindo categorias do painel de controle](assigning-control-panel-categories.md) para possíveis valores de categoria.</span><span class="sxs-lookup"><span data-stu-id="6eec1-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="6eec1-149">**System. software. TasksFileUrl**.</span><span class="sxs-lookup"><span data-stu-id="6eec1-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="6eec1-150">REG \_ sz ou reg \_ expande \_ sz.</span><span class="sxs-lookup"><span data-stu-id="6eec1-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="6eec1-151">O caminho do arquivo XML que define os [links de tarefas](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="6eec1-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="6eec1-152">Isso pode ser um caminho de arquivo direto, conforme mostrado no exemplo, ou um recurso inserido especificado como um nome de módulo e uma ID de recurso, como "% ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".</span><span class="sxs-lookup"><span data-stu-id="6eec1-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="6eec1-153">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="6eec1-153">Step 4:</span></span>

<span data-ttu-id="6eec1-154">Na mesma subchave GUID, adicione a seguinte subchave ao registro para fornecer o caminho do arquivo que contém o ícone e a ID de recurso da imagem dentro desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="6eec1-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="6eec1-155">Observe que, embora a sintaxe seja semelhante às entradas localizadas e InfoTip discutidas anteriormente, nenhum caractere ' @ ' é usado como um prefixo na entrada REG \_ sz ou reg \_ expande- \_ sz que especifica o caminho.</span><span class="sxs-lookup"><span data-stu-id="6eec1-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="6eec1-156">Etapa 5:</span><span class="sxs-lookup"><span data-stu-id="6eec1-156">Step 5:</span></span>

<span data-ttu-id="6eec1-157">Adicione as seguintes informações ao registro para fornecer o comando que é chamado pelo sistema quando o usuário abre o painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6eec1-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="6eec1-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6eec1-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eec1-159">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="6eec1-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6eec1-160">Como registrar itens do painel de controle da DLL</span><span class="sxs-lookup"><span data-stu-id="6eec1-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



