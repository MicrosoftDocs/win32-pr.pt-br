---
description: Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo. Como todos esses manipuladores, eles são objetos COM (Component Object Model) em processo implementados como DLLs.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Criando manipuladores de menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "103837534"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="f2bbd-104">Criando manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="f2bbd-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="f2bbd-105">Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="f2bbd-106">Como todos esses manipuladores, eles são objetos COM (Component Object Model) em processo implementados como DLLs.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="f2bbd-107">Há considerações especiais para o Windows de 64 bits ao registrar manipuladores que funcionam no contexto de aplicativos de 32 bits: quando os verbos do shell são invocados no contexto de um aplicativo de 32 bits, o subsistema WOW64 redireciona o acesso ao sistema de arquivos para alguns caminhos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="f2bbd-108">Se o manipulador. exe for armazenado em um desses caminhos, ele não estará acessível neste contexto.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="f2bbd-109">Portanto, como uma solução alternativa, armazene seu. exe em um caminho que não seja redirecionado ou armazene uma versão de stub do seu. exe que inicia a versão real.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="f2bbd-110">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f2bbd-111">Verbos canônicos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="f2bbd-112">Verbos estendidos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="f2bbd-113">Personalizando um menu de atalho usando verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="f2bbd-114">Ativando o manipulador usando a interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="f2bbd-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="f2bbd-115">Especificando a posição e a ordem de verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="f2bbd-116">Posicionando verbos na parte superior ou inferior do menu</span><span class="sxs-lookup"><span data-stu-id="f2bbd-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="f2bbd-117">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="f2bbd-118">Obtendo comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="f2bbd-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="f2bbd-119">Preterido: Associação de verbos com comandos troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="f2bbd-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="f2bbd-120">Concluindo tarefas de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="f2bbd-121">Personalizando o menu de atalho para objetos shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="f2bbd-122">Estendendo um novo submenu</span><span class="sxs-lookup"><span data-stu-id="f2bbd-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="f2bbd-123">Suprimindo verbos e controlando a visibilidade</span><span class="sxs-lookup"><span data-stu-id="f2bbd-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="f2bbd-124">Empregando o modelo de seleção de verbo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="f2bbd-125">Usando atributos de item</span><span class="sxs-lookup"><span data-stu-id="f2bbd-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="f2bbd-126">Implementando verbos personalizados para pastas por meio de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="f2bbd-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="f2bbd-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2bbd-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="f2bbd-128">Verbos canônicos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-128">Canonical Verbs</span></span>

<span data-ttu-id="f2bbd-129">Os aplicativos são geralmente responsáveis por fornecer cadeias de caracteres de exibição localizadas para os verbos que eles definem.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="f2bbd-130">No entanto, para fornecer um grau de independência de idioma, o sistema define um conjunto padrão de verbos usados comumente chamados de verbos canônicos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="f2bbd-131">Um verbo canônico nunca é exibido para o usuário e pode ser usado com qualquer idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="f2bbd-132">O sistema usa o nome canônico para gerar automaticamente uma cadeia de caracteres de exibição localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="f2bbd-133">Por exemplo, a cadeia de caracteres de exibição do verbo aberto é definida como **aberta** em um sistema em inglês e para o equivalente em alemão em um sistema alemão.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="f2bbd-134">Verbo canônico</span><span class="sxs-lookup"><span data-stu-id="f2bbd-134">Canonical verb</span></span> | <span data-ttu-id="f2bbd-135">Description</span><span class="sxs-lookup"><span data-stu-id="f2bbd-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="f2bbd-136">Aberto</span><span class="sxs-lookup"><span data-stu-id="f2bbd-136">Open</span></span>           | <span data-ttu-id="f2bbd-137">Abre o arquivo ou a pasta.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="f2bbd-138">Opennew</span><span class="sxs-lookup"><span data-stu-id="f2bbd-138">Opennew</span></span>        | <span data-ttu-id="f2bbd-139">Abre o arquivo ou a pasta em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="f2bbd-140">Imprimir</span><span class="sxs-lookup"><span data-stu-id="f2bbd-140">Print</span></span>          | <span data-ttu-id="f2bbd-141">Imprime o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="f2bbd-142">Imprimir em</span><span class="sxs-lookup"><span data-stu-id="f2bbd-142">Printto</span></span>        | <span data-ttu-id="f2bbd-143">Permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="f2bbd-144">Explorar</span><span class="sxs-lookup"><span data-stu-id="f2bbd-144">Explore</span></span>        | <span data-ttu-id="f2bbd-145">Abre o Windows Explorer com a pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="f2bbd-146">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2bbd-146">Properties</span></span>     | <span data-ttu-id="f2bbd-147">Abre a folha de propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="f2bbd-148">O verbo **Printto** também é canônico, mas nunca é exibido.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="f2bbd-149">Sua inclusão permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="f2bbd-150">Os manipuladores de menu de atalho podem fornecer seus próprios verbos canônicos por meio de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) com **GCS \_ VERBW** ou **GCS \_ verba**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="f2bbd-151">O sistema usará os verbos canônicos como o segundo parâmetro (*lpOperation*) passado para [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e será o [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membro **lpVerb** passado para o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="f2bbd-152">Verbos estendidos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-152">Extended Verbs</span></span>

<span data-ttu-id="f2bbd-153">Quando o usuário clica com o botão direito do mouse em um objeto, o menu de atalho exibe os verbos padrão.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="f2bbd-154">Talvez você queira adicionar e dar suporte a comandos em alguns menus de atalho que não são exibidos em todos os menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="f2bbd-155">Por exemplo, você pode ter comandos que não são comumente usados ou que se destinam a usuários experientes.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="f2bbd-156">Por esse motivo, você também pode definir um ou mais verbos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="f2bbd-157">Esses verbos são semelhantes aos verbos normais, mas são diferenciados de verbos normais pela maneira como são registrados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="f2bbd-158">Para ter acesso a verbos estendidos, o usuário deve clicar com o botão direito do mouse em um objeto enquanto pressiona a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="f2bbd-159">Quando o usuário faz isso, os verbos estendidos são exibidos além dos verbos padrão.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="f2bbd-160">Você pode usar o registro para definir um ou mais verbos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="f2bbd-161">Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto e também pressionar a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="f2bbd-162">Para definir um verbo como estendido, adicione um valor de **\_ sz reg** "estendido" à subchave do verbo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="f2bbd-163">O valor não deve ter nenhum dado associado a ele.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="f2bbd-164">Personalizando um menu de atalho usando verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="f2bbd-165">Depois de [escolher um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md) , você pode estender o menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="f2bbd-166">Para fazer isso, adicione uma subchave de **shell** abaixo da subchave do ProgID do aplicativo associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="f2bbd-167">Opcionalmente, você pode definir um verbo padrão para o tipo de arquivo, tornando-o o valor padrão da subchave **shell** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="f2bbd-168">O verbo padrão é exibido primeiro no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="f2bbd-169">Seu objetivo é fornecer ao shell um verbo que possa ser usado quando a função [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) for chamada, mas nenhum verbo for especificado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="f2bbd-170">O shell não seleciona necessariamente o verbo padrão quando **ShellExecuteEx** é usado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="f2bbd-171">O Shell usa o primeiro verbo disponível na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="f2bbd-172">O verbo padrão</span><span class="sxs-lookup"><span data-stu-id="f2bbd-172">The default verb</span></span>
2.  <span data-ttu-id="f2bbd-173">O primeiro verbo no registro, se a ordem de verbo for especificada</span><span class="sxs-lookup"><span data-stu-id="f2bbd-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="f2bbd-174">O verbo **abrir**</span><span class="sxs-lookup"><span data-stu-id="f2bbd-174">The **Open** verb</span></span>
4.  <span data-ttu-id="f2bbd-175">O verbo **abrir com**</span><span class="sxs-lookup"><span data-stu-id="f2bbd-175">The **Open With** verb</span></span>

<span data-ttu-id="f2bbd-176">Se nenhum dos verbos listados estiver disponível, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="f2bbd-177">Crie uma subchave para cada verbo que você deseja adicionar na subchave do Shell.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="f2bbd-178">Cada uma dessas subchaves deve ter um valor **reg \_ sz** definido como a cadeia de caracteres de exibição do verbo (cadeia de caracteres localizada).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="f2bbd-179">Para cada subchave de verbo, crie uma subchave de comando com o valor padrão definido para a linha de comando para ativar os itens.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="f2bbd-180">Para verbos canônicos, como **abrir** e **Imprimir**, você pode omitir a cadeia de caracteres de exibição porque o sistema exibe automaticamente uma cadeia de caracteres localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="f2bbd-181">Para verbos noncanonal, se você omitir a cadeia de caracteres de exibição, a cadeia de caracteres de verbo será exibida.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="f2bbd-182">No exemplo de registro a seguir, observe que:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="f2bbd-183">Como **doit** não é um verbo canônico, ele recebe um nome de exibição, que pode ser selecionado pressionando a tecla D.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="f2bbd-184">O verbo **Printto** não aparece no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="f2bbd-185">No entanto, sua inclusão no registro permite que o usuário imprima arquivos soltando-os em um ícone de impressora.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="f2bbd-186">Uma subchave é mostrada para cada verbo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="f2bbd-187">**%1** representa o nome do arquivo e **%2** o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-187">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="f2bbd-188">O diagrama a seguir ilustra a extensão do menu de atalho de acordo com as entradas de registro acima.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="f2bbd-189">Este **menu de atalho abriu**, **faz** e **imprime** verbos em seu menu, com o que **é** o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![captura de tela do menu de atalho do verbo padrão](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="f2bbd-191">Ativando o manipulador usando a interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="f2bbd-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="f2bbd-192">O troca dinâmica de dados (DDE) foi preterido; Use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="f2bbd-193">O **IDropTarget** é mais robusto e tem melhor suporte à ativação porque usa a ativação com do manipulador.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="f2bbd-194">No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho de buffer encontradas no DDE e no [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="f2bbd-195">Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="f2bbd-196">Fazer isso é mais simples e não perde as informações de namespace, pois ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="f2bbd-197">Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="f2bbd-198">Especificando a posição e a ordem de verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="f2bbd-199">Normalmente, os verbos são ordenados em um menu de atalho com base em como são enumerados; a enumeração é baseada primeiro na ordem da matriz de associação e, em seguida, na ordem dos itens na matriz de associação, conforme definido pela ordem de classificação do registro.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="f2bbd-200">Os verbos podem ser ordenados especificando o valor padrão da subchave Shell para a entrada de associação.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="f2bbd-201">Esse valor padrão pode incluir um único item, que será exibido na posição superior do menu de atalho ou uma lista de itens separados por espaços ou vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="f2bbd-202">No último caso, o primeiro item na lista é o item padrão e os outros verbos são exibidos imediatamente abaixo dele na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="f2bbd-203">Por exemplo, a seguinte entrada de registro produz verbos de menu de atalho na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="f2bbd-204">Monitor</span><span class="sxs-lookup"><span data-stu-id="f2bbd-204">Display</span></span>
2.  <span data-ttu-id="f2bbd-205">Miniaplicativo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-205">Gadgets</span></span>
3.  <span data-ttu-id="f2bbd-206">Personalização</span><span class="sxs-lookup"><span data-stu-id="f2bbd-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="f2bbd-207">Da mesma forma, a seguinte entrada de registro produz verbos de menu de atalho na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="f2bbd-208">Personalização</span><span class="sxs-lookup"><span data-stu-id="f2bbd-208">Personalization</span></span>
2.  <span data-ttu-id="f2bbd-209">Miniaplicativo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-209">Gadgets</span></span>
3.  <span data-ttu-id="f2bbd-210">Monitor</span><span class="sxs-lookup"><span data-stu-id="f2bbd-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="f2bbd-211">Posicionando verbos na parte superior ou inferior do menu</span><span class="sxs-lookup"><span data-stu-id="f2bbd-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="f2bbd-212">O atributo de registro a seguir pode ser usado para posicionar um verbo na parte superior ou inferior do menu.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="f2bbd-213">Se houver vários verbos que especifiquem esse atributo, o último a fazer isso obterá a prioridade:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="f2bbd-214">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="f2bbd-215">No Windows 7 e posterior, há suporte para implementação de menu em cascata por meio das configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="f2bbd-216">Antes do Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="f2bbd-217">No Windows 7 e posterior, você deve recorrer a soluções baseadas em código COM somente quando os métodos estáticos forem insuficientes.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="f2bbd-218">A captura de tela a seguir fornece um exemplo de um menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-218">The following screen shot provides an example of a cascading menu.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="f2bbd-220">No Windows 7 e posterior, há três maneiras de criar menus em cascata:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="f2bbd-221">Criando menus em cascata com a entrada de registro de subcomandos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="f2bbd-222">Criando menus em cascata com a entrada de registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="f2bbd-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="f2bbd-223">Criando menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="f2bbd-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="f2bbd-224">Criando menus em cascata com a entrada de registro de subcomandos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="f2bbd-225">No Windows 7 e posterior, você pode usar a entrada subcomandos para criar menus em cascata usando o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="f2bbd-226">**Para criar um menu em cascata usando a entrada de subcomandos**</span><span class="sxs-lookup"><span data-stu-id="f2bbd-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="f2bbd-227">Crie uma subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell** para representar o menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="f2bbd-228">Neste exemplo, damos a essa subchave o nome *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="f2bbd-229">Verifique se o valor padrão da subchave *CascadeTest* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="f2bbd-230">Para sua subchave *CascadeTest* , adicione uma entrada MUIVerb do tipo **reg \_ sz** e atribua a ela o texto que será exibido como seu nome no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="f2bbd-231">Neste exemplo, atribuímos "menu de teste em cascata".</span><span class="sxs-lookup"><span data-stu-id="f2bbd-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="f2bbd-232">Para a subchave *CascadeTest* , adicione uma entrada subcomandos do tipo **reg \_ sz** que é atribuído à lista, demlimited por ponto e vírgula, dos verbos que devem aparecer no menu, na ordem de aparência.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="f2bbd-233">Por exemplo, aqui, atribuímos vários verbos fornecidos pelo sistema:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="f2bbd-234">No caso de verbos personalizados, implemente-os usando qualquer um dos métodos de implementação de verbo estático e liste-os na subchave **CommandStore** , conforme mostrado neste exemplo para um verbo fictício *verbalname*:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="f2bbd-235">Esse método tem a vantagem de que os verbos personalizados podem ser registrados uma vez e reutilizados, listando o nome do verbo na entrada subcomandos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="f2bbd-236">No entanto, ele requer que o aplicativo tenha permissão para modificar o registro em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="f2bbd-237">Criando menus em cascata com a entrada de registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="f2bbd-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="f2bbd-238">No Windows 7 e posterior, você pode usar a entrada ExtendedSubCommandKey para criar menus em cascata estendidos: menus em cascata dentro de menus em cascata.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="f2bbd-239">A captura de tela a seguir é um exemplo de um menu estendido em cascata.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-239">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de tela mostrando o menu em cascata estendida para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="f2bbd-241">Como **a \_ \_ raiz das classes hKey** é uma combinação de **HKEY \_ Current \_ User** e **HKEY \_ local \_ Machine**, você pode registrar qualquer verbo personalizado na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="f2bbd-242">A principal vantagem disso é que a permissão elevada não é necessária.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="f2bbd-243">Além disso, outras associações de arquivo podem reutilizar esse conjunto inteiro de verbos especificando a mesma subchave ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="f2bbd-244">Se você não precisar reutilizar esse conjunto de verbos, poderá listar os verbos sob o pai, mas certifique-se de que o valor padrão do pai esteja vazio.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="f2bbd-245">**Para criar um menu em cascata usando uma entrada ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="f2bbd-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="f2bbd-246">Crie uma subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell** para representar o menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="f2bbd-247">Neste exemplo, damos a essa subchave o nome *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="f2bbd-248">Verifique se o valor padrão da subchave *CascadeTest* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="f2bbd-249">Para sua subchave *CascadeTest* , adicione uma entrada MUIVerb do tipo **reg \_ sz** e atribua a ela o texto que será exibido como seu nome no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="f2bbd-250">Neste exemplo, atribuímos "menu de teste em cascata".</span><span class="sxs-lookup"><span data-stu-id="f2bbd-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="f2bbd-251">Na subchave *CascadeTest* que você criou, adicione uma subchave **ExtendedSubCommandsKey** e, em seguida, adicione os subcomandos de documento (do tipo **reg \_ sz** ); por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="f2bbd-252">Verifique se o valor padrão da subchave *Test Cascade do menu 2* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="f2bbd-253">Preencha os subverbos usando qualquer uma das seguintes implementações de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="f2bbd-254">Observe que a subchave CommandFlags representa os valores de EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="f2bbd-255">Se você quiser adicionar um separador antes ou depois do item de menu em cascata, use ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="f2bbd-256">Para obter uma descrição desses sinalizadores do Windows 7 e posterior, consulte [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="f2bbd-257">ECF \_ SEPARATORBEFORE funciona apenas para os itens de menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="f2bbd-258">MUIVerb é do tipo **reg \_ sz** e CommandFlags é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="f2bbd-259">A captura de tela a seguir é uma ilustração dos exemplos de entrada de chave do registro anterior.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata mostrando as opções do bloco de notas e do WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="f2bbd-261">Criando menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="f2bbd-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="f2bbd-262">Outra opção para adicionar verbos a um menu em cascata é por meio de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="f2bbd-263">Esse método habilita fontes de dados que fornecem seus comandos de módulo de comando por meio de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esses comandos como verbos em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="f2bbd-264">No Windows 7 e posterior, você pode fornecer a mesma implementação de verbo usando [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como você pode com o [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="f2bbd-265">As duas capturas de tela a seguir ilustram o uso de menus em cascata na pasta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="f2bbd-267">A captura de tela a seguir ilustra outra implementação de um menu em cascata na pasta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="f2bbd-269">Como o [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável para uso por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="f2bbd-270">Obtendo comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="f2bbd-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="f2bbd-271">A sintaxe de consulta avançada (AQS) pode expressar uma condição que será avaliada usando as propriedades do item para o qual o verbo está sendo instanciado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="f2bbd-272">Esse sistema funciona apenas com propriedades rápidas.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-272">This system works only with fast properties.</span></span> <span data-ttu-id="f2bbd-273">Essas são propriedades que a fonte de dados do Shell relata como rápido, não retornando [\* \* \* \* SHCOLSTATE \_ lento \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* de [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="f2bbd-274">O Windows 7 e versões posteriores dão suporte a valores canônicos que evitam problemas em compilações localizadas.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="f2bbd-275">A sintaxe canônica a seguir é necessária em compilações localizadas para aproveitar esse aprimoramento do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="f2bbd-276">Na seguinte entrada de registro de exemplo:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="f2bbd-277">O valor **AppliesTo** controla se o verbo é exibido ou oculto.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="f2bbd-278">O valor defaultappliestoto controla qual verbo é o padrão.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="f2bbd-279">O valor HasLUAShield controla se um escudo de controle de conta de usuário (UAC) é exibido.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="f2bbd-280">Neste exemplo, o valor **defaultappliesto** torna esse verbo o padrão para qualquer arquivo com a palavra "exampleText1" em seu nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="f2bbd-281">O valor **AppliesTo** habilita o verbo para qualquer arquivo com "exampleText1" no nome.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="f2bbd-282">O valor **HasLUAShield** exibe o escudo para arquivos com "exampleText2" no nome.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="f2bbd-283">Adicione a subchave de **comando** e um valor:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="f2bbd-284">No registro do Windows 7, consulte **HKEY \_ classes \_ raiz** \\ **drive** como um exemplo de verbos do BitLocker que empregam a seguinte abordagem:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="f2bbd-285">Aplica-se a = System. volume. BitlockerProtection: = 2</span><span class="sxs-lookup"><span data-stu-id="f2bbd-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="f2bbd-286">System. volume. BitlockerRequiresAdmin: = System. StructuredQueryType. booliano \# true</span><span class="sxs-lookup"><span data-stu-id="f2bbd-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="f2bbd-287">Para obter mais informações sobre AQS, consulte [sintaxe de consulta avançada](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="f2bbd-288">Preterido: Associação de verbos com comandos troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="f2bbd-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="f2bbd-289">O DDE foi preterido; Use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="f2bbd-290">O DDE é preterido porque depende de uma mensagem de janela de difusão para descobrir o servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="f2bbd-291">Um servidor DDE trava a mensagem da janela de transmissão e, portanto, trava as conversas DDE para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="f2bbd-292">É comum que um único aplicativo preso cause falhas subsequentes em toda a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="f2bbd-293">O método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) é mais robusto e tem melhor suporte à ativação porque usa a ativação com do manipulador.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="f2bbd-294">No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho de buffer encontradas no DDE e no [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="f2bbd-295">Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="f2bbd-296">Fazer isso é mais simples e não perde as informações de namespace, pois ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="f2bbd-297">Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="f2bbd-298">Concluindo tarefas de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="f2bbd-299">As tarefas a seguir para implementar verbos são relevantes para as implementações de verbo estáticos e dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="f2bbd-300">Para obter mais informações sobre verbos dinâmicos, consulte [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="f2bbd-301">Personalizando o menu de atalho para objetos shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="f2bbd-302">Muitos objetos de shell predefinidos têm menus de atalho que podem ser personalizados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="f2bbd-303">Registre o comando praticamente da mesma maneira que você registra tipos de arquivo típicos, mas use o nome do objeto predefinido como o nome do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="f2bbd-304">Uma lista de objetos predefinidos está na seção *objetos do Shell predefinidos* da [criação de manipuladores de extensão do Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="f2bbd-305">Esses objetos de shell predefinidos cujos menus de atalho podem ser personalizados com a adição de verbos no registro são marcados na tabela com o verbo do Word.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="f2bbd-306">Estendendo um novo submenu</span><span class="sxs-lookup"><span data-stu-id="f2bbd-306">Extending a New Submenu</span></span>

<span data-ttu-id="f2bbd-307">Quando um usuário abre o menu **arquivo** no Windows Explorer, um dos comandos exibidos é **novo**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="f2bbd-308">A seleção desse comando exibe um submenu.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="f2bbd-309">Por padrão, o submenu contém dois comandos, **pasta** e **atalho**, que permitem aos usuários criar subpastas e atalhos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="f2bbd-310">Esse submenu pode ser estendido para incluir comandos de criação de arquivo para qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="f2bbd-311">Para adicionar um comando de criação de arquivo ao **novo** submenu, os arquivos do aplicativo devem ter um tipo de arquivo associado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="f2bbd-312">Inclua uma subchave **ShellNew** sob o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="f2bbd-313">Quando o comando **novo** do menu **arquivo** é selecionado, o Shell adiciona o tipo de arquivo ao **novo** submenu.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="f2bbd-314">A cadeia de caracteres de exibição do comando é a cadeia de caracteres descritiva que é atribuída ao ProgID do programa.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="f2bbd-315">Para especificar o método de criação de arquivo, atribua um ou mais valores de dados à subchave **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="f2bbd-316">Os valores disponíveis são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="f2bbd-317">Valor da subchave ShellNew</span><span class="sxs-lookup"><span data-stu-id="f2bbd-317">ShellNew subkey value</span></span> | <span data-ttu-id="f2bbd-318">Description</span><span class="sxs-lookup"><span data-stu-id="f2bbd-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bbd-319">Comando</span><span class="sxs-lookup"><span data-stu-id="f2bbd-319">Command</span></span>               | <span data-ttu-id="f2bbd-320">Executa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-320">Executes an application.</span></span> <span data-ttu-id="f2bbd-321">Esse valor **reg \_ sz** especifica o caminho do aplicativo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="f2bbd-322">Por exemplo, você pode defini-lo para iniciar um assistente.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="f2bbd-323">Dados</span><span class="sxs-lookup"><span data-stu-id="f2bbd-323">Data</span></span>                  | <span data-ttu-id="f2bbd-324">Cria um arquivo que contém os dados especificados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-324">Creates a file containing specified data.</span></span> <span data-ttu-id="f2bbd-325">Esse **valor \_ binário reg** especifica os dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="f2bbd-326">**Os dados** serão ignorados se **Nullfile** ou **filename** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="f2bbd-327">FileName</span><span class="sxs-lookup"><span data-stu-id="f2bbd-327">FileName</span></span>              | <span data-ttu-id="f2bbd-328">Cria um arquivo que é uma cópia de um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="f2bbd-329">Esse valor **reg \_ sz** especifica o caminho totalmente qualificado do arquivo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="f2bbd-330">Valor nulo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-330">NullFile</span></span>              | <span data-ttu-id="f2bbd-331">Cria um arquivo vazio.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-331">Creates an empty file.</span></span> <span data-ttu-id="f2bbd-332">**Nullfile** não tem um valor atribuído.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="f2bbd-333">Se **Nullfile** for especificado, os valores de registro de **Data** e **filename** serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="f2bbd-334">O exemplo de chave do registro a seguir e captura de tela ilustram o **novo** submenu para o tipo de arquivo. MYP-MS.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="f2bbd-335">Ele tem um comando, **aplicativo myprogram**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="f2bbd-336">A captura de tela ilustra o **novo** submenu.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="f2bbd-337">Quando um usuário seleciona o **aplicativo myprogram** no **novo** submenu, o Shell cria um arquivo chamado **novo myprogram Application. MYP-ms** e o passa para **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![captura de tela do Windows Explorer mostrando um novo comando "aplicativo myprogram" no submenu "novo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="f2bbd-339">Criando manipuladores do tipo "arrastar e soltar"</span><span class="sxs-lookup"><span data-stu-id="f2bbd-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="f2bbd-340">O procedimento básico para implementar um manipulador de arrastar e soltar é o mesmo que para manipuladores de menu de atalho convencionais.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="f2bbd-341">No entanto, os manipuladores de menu de atalho normalmente usam apenas o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passado para o método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) do manipulador para extrair o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="f2bbd-342">Um manipulador de arrastar e soltar pode implementar um manipulador de dados mais sofisticado para modificar o comportamento do objeto arrastado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="f2bbd-343">Quando um usuário clica com o botão direito do mouse em um objeto Shell para arrastar um objeto, um menu de atalho é exibido quando o usuário tenta descartar o objeto.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="f2bbd-344">A captura de tela a seguir ilustra um menu de atalho típico do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="f2bbd-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![captura de tela do menu de atalho arrastar e soltar](images/context-menu/context-dragdrop.png)

<span data-ttu-id="f2bbd-346">Um manipulador de arrastar e soltar é um manipulador de menu de atalho que pode adicionar itens a esse menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="f2bbd-347">Os manipuladores de arrastar e soltar normalmente são registrados na subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="f2bbd-348">Adicione uma subchave sob a subchave **DragDropHandlers** chamada para o manipulador de arrastar e soltar e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="f2bbd-349">O exemplo a seguir habilita o manipulador de arrastar e soltar **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="f2bbd-350">Suprimindo verbos e controlando a visibilidade</span><span class="sxs-lookup"><span data-stu-id="f2bbd-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="f2bbd-351">Você pode usar as configurações da política do Windows para controlar a visibilidade do verbo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="f2bbd-352">Os verbos podem ser suprimidos por meio de configurações de política adicionando um valor de **SuppressionPolicy** ou um valor de GUID **SuppressionPolicyEx** à subchave do registro do verbo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="f2bbd-353">Defina o valor da subchave **SuppressionPolicy** para a ID da política.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="f2bbd-354">Se a política for ativada, o verbo e sua entrada de menu de atalho associada serão suprimidos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="f2bbd-355">Para obter possíveis valores de ID de política, consulte a enumeração de [**restrições**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="f2bbd-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="f2bbd-356">Empregando o modelo de seleção de verbo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="f2bbd-357">Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="f2bbd-358">Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="f2bbd-359">Os valores possíveis para o modelo de seleção de verbo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="f2bbd-360">Especifique o valor de MultiSelectModel para todos os verbos.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="f2bbd-361">Se o valor de MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="f2bbd-362">Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, o **documento** é assumido.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="f2bbd-363">Especifique **single** para verbos que dão suporte a apenas uma única seleção.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="f2bbd-364">Especifique o **Player** para verbos que dão suporte a qualquer número de itens.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="f2bbd-365">Especifique o **documento** para verbos que criam uma janela de nível superior para cada item.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="f2bbd-366">Isso limita o número de itens ativados e ajuda a evitar a execução de recursos do sistema se o usuário abrir muitas janelas.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="f2bbd-367">Quando o número de itens selecionados não corresponde ao modelo de seleção de verbo ou é maior que os limites padrão descritos na tabela a seguir, o verbo não aparece.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="f2bbd-368">Tipo de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-368">Type of verb implementation</span></span> | <span data-ttu-id="f2bbd-369">Documento</span><span class="sxs-lookup"><span data-stu-id="f2bbd-369">Document</span></span> | <span data-ttu-id="f2bbd-370">Jogador</span><span class="sxs-lookup"><span data-stu-id="f2bbd-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="f2bbd-371">Herdada</span><span class="sxs-lookup"><span data-stu-id="f2bbd-371">Legacy</span></span>                      | <span data-ttu-id="f2bbd-372">15 itens</span><span class="sxs-lookup"><span data-stu-id="f2bbd-372">15 items</span></span> | <span data-ttu-id="f2bbd-373">100 itens</span><span class="sxs-lookup"><span data-stu-id="f2bbd-373">100 items</span></span> |
| <span data-ttu-id="f2bbd-374">COM</span><span class="sxs-lookup"><span data-stu-id="f2bbd-374">COM</span></span>                         | <span data-ttu-id="f2bbd-375">15 itens</span><span class="sxs-lookup"><span data-stu-id="f2bbd-375">15 items</span></span> | <span data-ttu-id="f2bbd-376">Sem limite</span><span class="sxs-lookup"><span data-stu-id="f2bbd-376">No limit</span></span>  |



 

<span data-ttu-id="f2bbd-377">Veja a seguir as entradas de registro de exemplo usando o valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-377">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="f2bbd-378">Usando atributos de item</span><span class="sxs-lookup"><span data-stu-id="f2bbd-378">Using Item Attributes</span></span>

<span data-ttu-id="f2bbd-379">Os valores de sinalizador [**SFGAO**](sfgao.md) dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="f2bbd-380">Para usar esse recurso de atributo, adicione os seguintes valores de **reg \_ DWORD** no verbo:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="f2bbd-381">O valor AttributeMask especifica o valor de [**SFGAO**](sfgao.md) dos valores de bits da máscara com a qual testar.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="f2bbd-382">O valor AttributeValue especifica o valor [**SFGAO**](sfgao.md) dos bits que são testados.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="f2bbd-383">O ImpliedSelectionModel Especifica zero para verbos de item ou zero para verbos no menu de atalho de segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="f2bbd-384">Na entrada de registro de exemplo a seguir, o AttributeMask é definido como [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="f2bbd-385">Implementando verbos personalizados para pastas por meio de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="f2bbd-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="f2bbd-386">No Windows 7 e posterior, você pode adicionar verbos a uma pasta por meio de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="f2bbd-387">Para obter mais informações sobre Desktop.ini arquivos, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="f2bbd-388">Desktop.ini arquivos devem ser sempre marcados como ocultos do **sistema** para que  +   não sejam exibidos aos usuários.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="f2bbd-389">**Para adicionar verbos personalizados para pastas por meio de um arquivo Desktop.ini, execute as seguintes etapas:**</span><span class="sxs-lookup"><span data-stu-id="f2bbd-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="f2bbd-390">Crie uma pasta que esteja marcada como **somente leitura** ou **sistema**.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="f2bbd-391">Crie um arquivo de Desktop.ini que inclui um \[ . ShellClassInfo \] DirectoryClass = ProgID da pasta.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="f2bbd-392">No registro, crie o ProgID da pasta **\_ \_ raiz das classes hKey** \\  com um valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="f2bbd-393">O valor CanUseForDirectory evita o uso indevido de ProgIDs que estão definidos para não participar da implementação de verbos personalizados para pastas por meio de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="f2bbd-394">Adicione verbos na subchave ProgID da **pasta**, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="f2bbd-395">Esses verbos podem ser o verbo padrão; nesse caso, clicar duas vezes na pasta ativa o verbo.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f2bbd-396">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2bbd-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bbd-397">Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="f2bbd-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-398">Escolhendo um verbo estático ou dinâmico para o menu de atalho</span><span class="sxs-lookup"><span data-stu-id="f2bbd-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-399">Personalizando um menu de atalho usando verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="f2bbd-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-400">Menus de atalho (contexto) e manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="f2bbd-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-401">Verbos e associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="f2bbd-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-402">Referência do menu de atalho</span><span class="sxs-lookup"><span data-stu-id="f2bbd-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
