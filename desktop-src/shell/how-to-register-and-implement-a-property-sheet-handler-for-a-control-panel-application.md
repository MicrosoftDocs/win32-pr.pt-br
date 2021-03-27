---
description: Muitos aplicativos do painel de controle exibem uma folha de propriedades de propriedades para permitir que os usuários exibam e modifiquem várias configurações do dispositivo e do sistema.
title: Como registrar e implementar um manipulador de folha de propriedades para um aplicativo do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828288"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3744d-103">Como registrar e implementar um manipulador de folha de propriedades para um aplicativo do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3744d-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3744d-104">Muitos aplicativos do painel de controle exibem uma folha de propriedades de propriedades para permitir que os usuários exibam e modifiquem várias configurações do dispositivo e do sistema.</span><span class="sxs-lookup"><span data-stu-id="3744d-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="3744d-105">Dois desses aplicativos — mouse e exibição — permitem que manipuladores de folha de propriedades substituam uma ou mais de suas páginas por uma página personalizada.</span><span class="sxs-lookup"><span data-stu-id="3744d-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="3744d-106">A captura de tela a seguir mostra a folha de propriedades **Propriedades do mouse** .</span><span class="sxs-lookup"><span data-stu-id="3744d-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![folha de propriedades propriedades do mouse](images/propsheethandler3.jpg)

<span data-ttu-id="3744d-108">Os manipuladores de folha de propriedades para aplicativos do painel de controle são semelhantes aos tipos de arquivo, com duas exceções principais:</span><span class="sxs-lookup"><span data-stu-id="3744d-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="3744d-109">Eles são chamados por um aplicativo do painel de controle, não pelo shell.</span><span class="sxs-lookup"><span data-stu-id="3744d-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="3744d-110">Elas são registradas de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="3744d-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3744d-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="3744d-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3744d-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="3744d-112">Technologies</span></span>

-   <span data-ttu-id="3744d-113">Shell</span><span class="sxs-lookup"><span data-stu-id="3744d-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3744d-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="3744d-114">Prerequisites</span></span>

-   <span data-ttu-id="3744d-115">Uma compreensão do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3744d-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="3744d-116">Uma compreensão dos menus de atalho</span><span class="sxs-lookup"><span data-stu-id="3744d-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="3744d-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="3744d-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3744d-118">Etapa 1: registrar um manipulador de folha de propriedades para um aplicativo do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3744d-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3744d-119">Um manipulador de folhas de propriedades do aplicativo do painel de controle deve ser registrado na subchave do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3744d-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="3744d-120">Essa chave pode estar em um dos dois locais, dependendo se o manipulador deve ser por usuário ou por computador.</span><span class="sxs-lookup"><span data-stu-id="3744d-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="3744d-121">Para o registro por usuário, a subchave do painel de controle é **HKEY \_ Current \_ User** \\ **Control painel**.</span><span class="sxs-lookup"><span data-stu-id="3744d-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="3744d-122">A macro REGSTR \_ Path \_ CONTROLPANEL, conforme definido em REGSTR. h, pode ser usada no código no lugar de "painel de controle".</span><span class="sxs-lookup"><span data-stu-id="3744d-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="3744d-123">Para o registro por computador, o local é:</span><span class="sxs-lookup"><span data-stu-id="3744d-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="3744d-124">Esse caminho pode ser referenciado no código como HKEY \_ local \_ Machine \\ REGSTR \_ Path \_ CONTROLSFOLDER, usando a \_ macro REGSTR Path \_ CONTROLSFOLDER que é definida em REGSTR. h.</span><span class="sxs-lookup"><span data-stu-id="3744d-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="3744d-125">Os aplicativos do painel de controle que permitem que os manipuladores de folhas de propriedades substituam páginas têm uma subchave na subchave do painel de controle, nomeada para o aplicativo, como mouse e exibição.</span><span class="sxs-lookup"><span data-stu-id="3744d-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="3744d-126">A subchave do aplicativo deve ter uma subchave **shellex** com uma subchave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="3744d-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="3744d-127">Para registrar um manipulador de folha de propriedades, adicione seu GUID à subchave **PropertySheetHandlers** que está associada ao aplicativo do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3744d-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="3744d-128">Para fazer isso, crie uma subchave da subchave **PropertySheetHandlers** , chamada para o manipulador de folha de propriedades, e defina seu valor padrão como a forma de cadeia de caracteres do GUID do manipulador.</span><span class="sxs-lookup"><span data-stu-id="3744d-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="3744d-129">O exemplo a seguir registra um manipulador de folha de propriedades para o aplicativo do painel de controle do mouse em uma base por computador.</span><span class="sxs-lookup"><span data-stu-id="3744d-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="3744d-130">Para registrá-lo em uma base por usuário, substitua **HKEY \_ local \_ Machine** \\ **REGSTR \_ caminho \_ CONTROLSFOLDER** com **HKEY \_ Current \_ User** \\ **REGSTR \_ Path \_ CONTROLPANEL**.</span><span class="sxs-lookup"><span data-stu-id="3744d-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3744d-131">Etapa 2: Implementando um manipulador de folha de propriedades para um aplicativo do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3744d-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3744d-132">O procedimento para implementar um manipulador de folhas de propriedades do painel de controle é muito semelhante ao que foi discutido em [como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="3744d-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="3744d-133">A principal diferença é que agora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) precisa de uma implementação não token em vez de [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="3744d-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="3744d-134">Quando um aplicativo do painel de controle está prestes a exibir sua folha de propriedades, ele chama o método [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) do manipulador de folhas de propriedades uma vez para cada página que pode ser substituída.</span><span class="sxs-lookup"><span data-stu-id="3744d-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="3744d-135">O parâmetro *uPageID* é definido como a ID da página.</span><span class="sxs-lookup"><span data-stu-id="3744d-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="3744d-136">As IDs para as páginas disponíveis são definidas em Cplext. h.</span><span class="sxs-lookup"><span data-stu-id="3744d-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="3744d-137">As IDs disponíveis no momento estão listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3744d-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="3744d-138">ID da página</span><span class="sxs-lookup"><span data-stu-id="3744d-138">Page ID</span></span>                      | <span data-ttu-id="3744d-139">Description</span><span class="sxs-lookup"><span data-stu-id="3744d-139">Description</span></span>         | <span data-ttu-id="3744d-140">Aplicativo do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3744d-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="3744d-141">CPLPAGE \_ botões de mouse \_</span><span class="sxs-lookup"><span data-stu-id="3744d-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="3744d-142">A página botões</span><span class="sxs-lookup"><span data-stu-id="3744d-142">The Buttons page</span></span>    | <span data-ttu-id="3744d-143">Mouse</span><span class="sxs-lookup"><span data-stu-id="3744d-143">Mouse</span></span>                     |
| <span data-ttu-id="3744d-144">CPLPAGE \_ mouse \_ PTRMOTION</span><span class="sxs-lookup"><span data-stu-id="3744d-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="3744d-145">A página de movimento</span><span class="sxs-lookup"><span data-stu-id="3744d-145">The Motion page</span></span>     | <span data-ttu-id="3744d-146">Mouse</span><span class="sxs-lookup"><span data-stu-id="3744d-146">Mouse</span></span>                     |
| <span data-ttu-id="3744d-147">\_roda do mouse CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="3744d-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="3744d-148">A página de roda</span><span class="sxs-lookup"><span data-stu-id="3744d-148">The Wheel page</span></span>      | <span data-ttu-id="3744d-149">Mouse</span><span class="sxs-lookup"><span data-stu-id="3744d-149">Mouse</span></span>                     |
| <span data-ttu-id="3744d-150">\_velocidade do teclado CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="3744d-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="3744d-151">A página velocidade</span><span class="sxs-lookup"><span data-stu-id="3744d-151">The Speed page</span></span>      | <span data-ttu-id="3744d-152">Keyboard</span><span class="sxs-lookup"><span data-stu-id="3744d-152">Keyboard</span></span>                  |
| <span data-ttu-id="3744d-153">\_tela de \_ fundo do CPLPAGE</span><span class="sxs-lookup"><span data-stu-id="3744d-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="3744d-154">A página de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="3744d-154">The Background page</span></span> | <span data-ttu-id="3744d-155">Monitor</span><span class="sxs-lookup"><span data-stu-id="3744d-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="3744d-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="3744d-156">Remarks</span></span>

<span data-ttu-id="3744d-157">O procedimento para criar e substituir uma página é idêntico ao da adição de uma página.</span><span class="sxs-lookup"><span data-stu-id="3744d-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="3744d-158">Para obter mais informações, consulte [como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="3744d-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



