---
description: Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo. Como todos esses manipuladores, eles são objetos COM (Component Object Model) em processo implementados como DLLs.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Criando manipuladores de menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd2611c492d517e9312ec2a4e1c95d7f1aa0fea
ms.sourcegitcommit: 05b3d7f137ef9bbddf4049215cb11d55b935997e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108800967"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="2b954-104">Criando manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="2b954-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="2b954-105">Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="2b954-106">Esses manipuladores podem ser impelmented de uma maneira que os cause carregar em seu próprio processo ou no Gerenciador, ou em outros processos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="2b954-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="2b954-107">Tome cuidado ao criar manipuladores em processo, pois eles podem causar danos ao processo que os carrega.</span><span class="sxs-lookup"><span data-stu-id="2b954-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="2b954-108">Há considerações especiais para versões com base em 64 bits do Windows ao registrar manipuladores que funcionam no contexto de aplicativos de 32 bits: quando invocado no contexto de um aplicativo de diferentes períodos de leitura, o subsistema WOW64 redireciona o acesso ao sistema de arquivos para alguns caminhos.</span><span class="sxs-lookup"><span data-stu-id="2b954-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="2b954-109">Se o manipulador. exe for armazenado em um desses caminhos, ele não estará acessível neste contexto.</span><span class="sxs-lookup"><span data-stu-id="2b954-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="2b954-110">Portanto, como uma solução alternativa, armazene seu. exe em um caminho que não seja redirecionado ou armazene uma versão de stub do seu. exe que inicia a versão real.</span><span class="sxs-lookup"><span data-stu-id="2b954-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="2b954-111">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b954-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2b954-112">Verbos canônicos</span><span class="sxs-lookup"><span data-stu-id="2b954-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="2b954-113">Verbos estendidos</span><span class="sxs-lookup"><span data-stu-id="2b954-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="2b954-114">Personalizando um menu de atalho usando verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-114">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="2b954-115">Ativando o manipulador usando a interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="2b954-115">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="2b954-116">Especificando a posição e a ordem de verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-116">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="2b954-117">Posicionando verbos na parte superior ou inferior do menu</span><span class="sxs-lookup"><span data-stu-id="2b954-117">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="2b954-118">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-118">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="2b954-119">Obtendo comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="2b954-119">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="2b954-120">Preterido: Associação de verbos com comandos troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="2b954-120">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="2b954-121">Concluindo tarefas de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="2b954-121">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="2b954-122">Personalização do menu de atalho para objetos shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="2b954-122">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="2b954-123">Estendendo um novo submenu</span><span class="sxs-lookup"><span data-stu-id="2b954-123">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="2b954-124">Suprimindo verbos e controlando a visibilidade</span><span class="sxs-lookup"><span data-stu-id="2b954-124">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="2b954-125">Empregando o modelo de seleção de verbos</span><span class="sxs-lookup"><span data-stu-id="2b954-125">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="2b954-126">Usando atributos de item</span><span class="sxs-lookup"><span data-stu-id="2b954-126">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="2b954-127">Implementando verbos personalizados para pastas por meio Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="2b954-127">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="2b954-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b954-128">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="2b954-129">Verbos canônicos</span><span class="sxs-lookup"><span data-stu-id="2b954-129">Canonical Verbs</span></span>

<span data-ttu-id="2b954-130">Os aplicativos geralmente são responsáveis por fornecer cadeias de caracteres de exibição localizadas para os verbos que eles definem.</span><span class="sxs-lookup"><span data-stu-id="2b954-130">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="2b954-131">No entanto, para fornecer um grau de independência de idioma, o sistema define um conjunto padrão de verbos comumente usados chamados verbos canônicos.</span><span class="sxs-lookup"><span data-stu-id="2b954-131">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="2b954-132">Um verbo canônico nunca é exibido para o usuário e pode ser usado com qualquer linguagem de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b954-132">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="2b954-133">O sistema usa o nome canônico para gerar automaticamente uma cadeia de caracteres de exibição localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="2b954-133">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="2b954-134">Por exemplo, a cadeia de caracteres  de exibição do verbo aberto é definida como Abrir em um sistema em inglês e como o equivalente alemão em um sistema alemão.</span><span class="sxs-lookup"><span data-stu-id="2b954-134">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="2b954-135">Verbo canônico</span><span class="sxs-lookup"><span data-stu-id="2b954-135">Canonical verb</span></span> | <span data-ttu-id="2b954-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b954-136">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="2b954-137">Aberto</span><span class="sxs-lookup"><span data-stu-id="2b954-137">Open</span></span>           | <span data-ttu-id="2b954-138">Abre o arquivo ou a pasta.</span><span class="sxs-lookup"><span data-stu-id="2b954-138">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="2b954-139">Opennew</span><span class="sxs-lookup"><span data-stu-id="2b954-139">Opennew</span></span>        | <span data-ttu-id="2b954-140">Abre o arquivo ou a pasta em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="2b954-140">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="2b954-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="2b954-141">Print</span></span>          | <span data-ttu-id="2b954-142">Imprime o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-142">Prints the file.</span></span>                                                     |
| <span data-ttu-id="2b954-143">Printto</span><span class="sxs-lookup"><span data-stu-id="2b954-143">Printto</span></span>        | <span data-ttu-id="2b954-144">Permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="2b954-144">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="2b954-145">Explorar</span><span class="sxs-lookup"><span data-stu-id="2b954-145">Explore</span></span>        | <span data-ttu-id="2b954-146">Abre o Windows Explorer com a pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="2b954-146">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="2b954-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b954-147">Properties</span></span>     | <span data-ttu-id="2b954-148">Abre a folha de propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="2b954-148">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="2b954-149">O verbo **Printto** também é canônico, mas nunca é exibido.</span><span class="sxs-lookup"><span data-stu-id="2b954-149">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="2b954-150">Sua inclusão permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="2b954-150">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="2b954-151">Os manipuladores de menu de atalho podem fornecer seus próprios verbos canônicos por meio de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) com **GCS \_ VERBW** ou **GCS \_ verba**.</span><span class="sxs-lookup"><span data-stu-id="2b954-151">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="2b954-152">O sistema usará os verbos canônicos como o segundo parâmetro (*lpOperation*) passado para [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e será o [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membro **lpVerb** passado para o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="2b954-152">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="2b954-153">Verbos estendidos</span><span class="sxs-lookup"><span data-stu-id="2b954-153">Extended Verbs</span></span>

<span data-ttu-id="2b954-154">Quando o usuário clica com o botão direito do mouse em um objeto, o menu de atalho exibe os verbos padrão.</span><span class="sxs-lookup"><span data-stu-id="2b954-154">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="2b954-155">Talvez você queira adicionar e dar suporte a comandos em alguns menus de atalho que não são exibidos em todos os menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-155">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="2b954-156">Por exemplo, você pode ter comandos que não são comumente usados ou que se destinam a usuários experientes.</span><span class="sxs-lookup"><span data-stu-id="2b954-156">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="2b954-157">Por esse motivo, você também pode definir um ou mais verbos estendidos.</span><span class="sxs-lookup"><span data-stu-id="2b954-157">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="2b954-158">Esses verbos são semelhantes aos verbos normais, mas são diferenciados de verbos normais pela maneira como são registrados.</span><span class="sxs-lookup"><span data-stu-id="2b954-158">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="2b954-159">Para ter acesso a verbos estendidos, o usuário deve clicar com o botão direito do mouse em um objeto enquanto pressiona a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="2b954-159">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="2b954-160">Quando o usuário faz isso, os verbos estendidos são exibidos além dos verbos padrão.</span><span class="sxs-lookup"><span data-stu-id="2b954-160">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="2b954-161">Você pode usar o registro para definir um ou mais verbos estendidos.</span><span class="sxs-lookup"><span data-stu-id="2b954-161">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="2b954-162">Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto e também pressionar a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="2b954-162">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="2b954-163">Para definir um verbo como estendido, adicione um valor de **\_ sz reg** "estendido" à subchave do verbo.</span><span class="sxs-lookup"><span data-stu-id="2b954-163">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="2b954-164">O valor não deve ter nenhum dado associado a ele.</span><span class="sxs-lookup"><span data-stu-id="2b954-164">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="2b954-165">Personalizando um menu de atalho usando verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-165">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="2b954-166">Depois de [escolher um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md) , você pode estender o menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-166">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="2b954-167">Para fazer isso, adicione uma **sub-chave** shell abaixo da sub-chave para o ProgID do aplicativo associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-167">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="2b954-168">Opcionalmente, você pode definir um verbo padrão para o tipo de arquivo tornando-o o valor padrão da **sub-chave** shell.</span><span class="sxs-lookup"><span data-stu-id="2b954-168">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="2b954-169">O verbo padrão é exibido primeiro no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-169">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="2b954-170">Sua finalidade é fornecer ao Shell um verbo que ele pode usar quando a [**função ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) é chamada, mas nenhum verbo é especificado.</span><span class="sxs-lookup"><span data-stu-id="2b954-170">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="2b954-171">O Shell não seleciona necessariamente o verbo padrão quando **ShellExecuteEx** é usado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="2b954-171">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="2b954-172">O Shell usa o primeiro verbo disponível na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="2b954-172">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="2b954-173">O verbo padrão</span><span class="sxs-lookup"><span data-stu-id="2b954-173">The default verb</span></span>
2.  <span data-ttu-id="2b954-174">O primeiro verbo no Registro, se a ordem do verbo for especificada</span><span class="sxs-lookup"><span data-stu-id="2b954-174">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="2b954-175">O **verbo** Open</span><span class="sxs-lookup"><span data-stu-id="2b954-175">The **Open** verb</span></span>
4.  <span data-ttu-id="2b954-176">O **verbo Abrir com**</span><span class="sxs-lookup"><span data-stu-id="2b954-176">The **Open With** verb</span></span>

<span data-ttu-id="2b954-177">Se nenhum dos verbos listados estiver disponível, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="2b954-177">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="2b954-178">Crie uma sub-chave para cada verbo que você deseja adicionar na sub-chave shell.</span><span class="sxs-lookup"><span data-stu-id="2b954-178">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="2b954-179">Cada uma dessas sub-chaves deve ter um **valor REG \_ SZ** definido como a cadeia de caracteres de exibição do verbo (cadeia de caracteres localizada).</span><span class="sxs-lookup"><span data-stu-id="2b954-179">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="2b954-180">Para cada subkey de verbo, crie uma sub-chave de comando com o valor padrão definido como a linha de comando para ativar os itens.</span><span class="sxs-lookup"><span data-stu-id="2b954-180">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="2b954-181">Para verbos canônicos, como **Abrir** e **Imprimir,** você pode omitir a cadeia de caracteres de exibição porque o sistema exibe automaticamente uma cadeia de caracteres localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="2b954-181">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="2b954-182">Para verbos não não ínteegóricos, se você omitir a cadeia de caracteres de exibição, a cadeia de caracteres do verbo será exibida.</span><span class="sxs-lookup"><span data-stu-id="2b954-182">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="2b954-183">No exemplo de Registro a seguir, observe que:</span><span class="sxs-lookup"><span data-stu-id="2b954-183">In the following registry example, note that:</span></span>

-   <span data-ttu-id="2b954-184">Como **Doit** não é um verbo canônico, ele recebe um nome de exibição, que pode ser selecionado pressionando a tecla D.</span><span class="sxs-lookup"><span data-stu-id="2b954-184">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="2b954-185">O **verbo Printto** não aparece no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-185">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="2b954-186">No entanto, sua inclusão no Registro permite que o usuário imprima arquivos, soltando-os em um ícone de impressora.</span><span class="sxs-lookup"><span data-stu-id="2b954-186">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="2b954-187">Uma subchave é mostrada para cada verbo.</span><span class="sxs-lookup"><span data-stu-id="2b954-187">One subkey is shown for each verb.</span></span> <span data-ttu-id="2b954-188">**%1** representa o nome do arquivo e **%2** o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="2b954-188">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="2b954-189">O diagrama a seguir ilustra a extensão do menu de atalho de acordo com as entradas de registro acima.</span><span class="sxs-lookup"><span data-stu-id="2b954-189">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="2b954-190">Este **menu de atalho abriu**, **faz** e **imprime** verbos em seu menu, com o que **é** o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="2b954-190">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![captura de tela do menu de atalho do verbo padrão](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="2b954-192">Ativando o manipulador usando a interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="2b954-192">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="2b954-193">O troca dinâmica de dados (DDE) foi preterido; Use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2b954-193">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="2b954-194">O **IDropTarget** é mais robusto e tem melhor suporte à ativação porque usa a ativação com do manipulador.</span><span class="sxs-lookup"><span data-stu-id="2b954-194">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="2b954-195">No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho de buffer encontradas no DDE e no [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="2b954-195">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="2b954-196">Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="2b954-196">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="2b954-197">Fazer isso é mais simples e não perde as informações de namespace, pois ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2b954-197">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="2b954-198">Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2b954-198">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="2b954-199">Especificando a posição e a ordem de verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-199">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="2b954-200">Normalmente, os verbos são ordenados em um menu de atalho com base em como são enumerados; a enumeração é baseada primeiro na ordem da matriz de associação e, em seguida, na ordem dos itens na matriz de associação, conforme definido pela ordem de classificação do registro.</span><span class="sxs-lookup"><span data-stu-id="2b954-200">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="2b954-201">Os verbos podem ser ordenados especificando o valor padrão da subchave Shell para a entrada de associação.</span><span class="sxs-lookup"><span data-stu-id="2b954-201">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="2b954-202">Esse valor padrão pode incluir um único item, que será exibido na posição superior do menu de atalho ou uma lista de itens separados por espaços ou vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2b954-202">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="2b954-203">No último caso, o primeiro item na lista é o item padrão e os outros verbos são exibidos imediatamente abaixo dele na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="2b954-203">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="2b954-204">Por exemplo, a seguinte entrada do Registro produz verbos de menu de atalho na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="2b954-204">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="2b954-205">Monitor</span><span class="sxs-lookup"><span data-stu-id="2b954-205">Display</span></span>
2.  <span data-ttu-id="2b954-206">Gadgets</span><span class="sxs-lookup"><span data-stu-id="2b954-206">Gadgets</span></span>
3.  <span data-ttu-id="2b954-207">Personalização</span><span class="sxs-lookup"><span data-stu-id="2b954-207">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="2b954-208">Da mesma forma, a seguinte entrada do Registro produz verbos de menu de atalho na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="2b954-208">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="2b954-209">Personalização</span><span class="sxs-lookup"><span data-stu-id="2b954-209">Personalization</span></span>
2.  <span data-ttu-id="2b954-210">Gadgets</span><span class="sxs-lookup"><span data-stu-id="2b954-210">Gadgets</span></span>
3.  <span data-ttu-id="2b954-211">Monitor</span><span class="sxs-lookup"><span data-stu-id="2b954-211">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="2b954-212">Posicionando verbos na parte superior ou inferior do menu</span><span class="sxs-lookup"><span data-stu-id="2b954-212">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="2b954-213">O atributo do Registro a seguir pode ser usado para colocar um verbo na parte superior ou inferior do menu.</span><span class="sxs-lookup"><span data-stu-id="2b954-213">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="2b954-214">Se houver vários verbos que especificam esse atributo, o último a fazer isso obtém prioridade:</span><span class="sxs-lookup"><span data-stu-id="2b954-214">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="2b954-215">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="2b954-215">Creating Static Cascading Menus</span></span>

<span data-ttu-id="2b954-216">No Windows 7 e posterior, há suporte para a implementação do menu em cascata por meio das configurações do Registro.</span><span class="sxs-lookup"><span data-stu-id="2b954-216">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="2b954-217">Antes do Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="2b954-217">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="2b954-218">No Windows 7 e posterior, você deve recorrer a soluções baseadas em código COM somente quando os métodos estáticos não são suficientes.</span><span class="sxs-lookup"><span data-stu-id="2b954-218">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="2b954-219">A captura de tela a seguir fornece um exemplo de um menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="2b954-219">The following screen shot provides an example of a cascading menu.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="2b954-221">No Windows 7 e posterior, há três maneiras de criar menus em cascata:</span><span class="sxs-lookup"><span data-stu-id="2b954-221">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="2b954-222">Criando menus em cascata com a entrada do Registro SubCommands</span><span class="sxs-lookup"><span data-stu-id="2b954-222">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="2b954-223">Criando menus em cascata com a entrada do Registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="2b954-223">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="2b954-224">Criando menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="2b954-224">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="2b954-225">Criando menus em cascata com a entrada do Registro SubCommands</span><span class="sxs-lookup"><span data-stu-id="2b954-225">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="2b954-226">No Windows 7 e posterior, você pode usar a entrada SubCommands para criar menus em cascata usando o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b954-226">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="2b954-227">**Para criar um menu em cascata usando a entrada de subcomandos**</span><span class="sxs-lookup"><span data-stu-id="2b954-227">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="2b954-228">Crie uma subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell** para representar o menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="2b954-228">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="2b954-229">Neste exemplo, damos a essa subchave o nome *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="2b954-229">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="2b954-230">Verifique se o valor padrão da subchave *CascadeTest* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="2b954-230">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="2b954-231">Para sua subchave *CascadeTest* , adicione uma entrada MUIVerb do tipo **reg \_ sz** e atribua a ela o texto que será exibido como seu nome no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-231">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="2b954-232">Neste exemplo, atribuímos "menu de teste em cascata".</span><span class="sxs-lookup"><span data-stu-id="2b954-232">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="2b954-233">Para a subchave *CascadeTest* , adicione uma entrada subcomandos do tipo **reg \_ sz** que é atribuído à lista, demlimited por ponto e vírgula, dos verbos que devem aparecer no menu, na ordem de aparência.</span><span class="sxs-lookup"><span data-stu-id="2b954-233">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="2b954-234">Por exemplo, aqui, atribuímos vários verbos fornecidos pelo sistema:</span><span class="sxs-lookup"><span data-stu-id="2b954-234">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="2b954-235">No caso de verbos personalizados, implemente-os usando qualquer um dos métodos de implementação de verbo estático e liste-os na subchave **CommandStore** , conforme mostrado neste exemplo para um verbo fictício *verbalname*:</span><span class="sxs-lookup"><span data-stu-id="2b954-235">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="2b954-236">Esse método tem a vantagem de que os verbos personalizados podem ser registrados uma vez e reutilizados, listando o nome do verbo na entrada subcomandos.</span><span class="sxs-lookup"><span data-stu-id="2b954-236">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="2b954-237">No entanto, ele requer que o aplicativo tenha permissão para modificar o registro em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="2b954-237">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="2b954-238">Criando menus em cascata com a entrada de registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="2b954-238">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="2b954-239">No Windows 7 e posterior, você pode usar a entrada ExtendedSubCommandKey para criar menus em cascata estendidos: menus em cascata dentro de menus em cascata.</span><span class="sxs-lookup"><span data-stu-id="2b954-239">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="2b954-240">A captura de tela a seguir é um exemplo de um menu estendido em cascata.</span><span class="sxs-lookup"><span data-stu-id="2b954-240">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de tela mostrando o menu em cascata estendida para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="2b954-242">Como **a \_ \_ raiz das classes hKey** é uma combinação de **HKEY \_ Current \_ User** e **HKEY \_ local \_ Machine**, você pode registrar qualquer verbo personalizado na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="2b954-242">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="2b954-243">A principal vantagem de fazer isso é que a permissão elevada não é necessária.</span><span class="sxs-lookup"><span data-stu-id="2b954-243">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="2b954-244">Além disso, outras associações de arquivo podem reutilizar todo esse conjunto de verbos especificando a mesma subkey ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="2b954-244">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="2b954-245">Se você não precisar reutilizar esse conjunto de verbos, poderá listar os verbos sob o pai, mas garantir que o valor Padrão do pai esteja vazio.</span><span class="sxs-lookup"><span data-stu-id="2b954-245">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="2b954-246">**Para criar um menu em cascata usando uma entrada ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="2b954-246">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="2b954-247">Crie uma sub-chave no shell progID raiz de CLASSES **\_ \_** \\ *HKEY* \\  para representar o menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="2b954-247">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="2b954-248">Neste exemplo, damos a essa sub-chave o nome *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="2b954-248">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="2b954-249">Verifique se o valor padrão da sub-chave *CascadeTest* está vazio e mostrado como **(valor não definido).**</span><span class="sxs-lookup"><span data-stu-id="2b954-249">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="2b954-250">À sub-chave *CascadeTest,* adicione uma entrada MUIVerb do tipo **REG \_ SZ** e atribua a ela o texto que será exibido como seu nome no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-250">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="2b954-251">Neste exemplo, atribuímos a ele "Testar Menu em Cascata".</span><span class="sxs-lookup"><span data-stu-id="2b954-251">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="2b954-252">Na sub-chave *CascadeTest* que você criou, adicione uma sub-chave **ExtendedSubCommandsKey** e adicione os subcommands do documento (do tipo **REG \_ SZ);** por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2b954-252">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="2b954-253">Verifique se o valor padrão da sub-chave *do Menu em Cascata de Teste 2* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="2b954-253">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="2b954-254">Preencha os subverbs usando qualquer uma das implementações de verbo estático a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b954-254">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="2b954-255">Observe que a sub-chave CommandFlags representa valores EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="2b954-255">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="2b954-256">Se você quiser adicionar um separador antes ou após o item de menu em cascata, use ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="2b954-256">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="2b954-257">Para obter uma descrição desses sinalizadores do Windows 7 e posterior, consulte [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="2b954-257">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="2b954-258">ECF \_ SEPARATORBEFORE funciona apenas para os itens de menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2b954-258">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="2b954-259">MUIVerb é do tipo **REG \_ SZ** e CommandFlags é do tipo **REG \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2b954-259">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="2b954-260">A captura de tela a seguir é uma ilustração dos exemplos de entrada de chave do Registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="2b954-260">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata mostrando opções de bloco de notas e wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="2b954-262">Criando menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="2b954-262">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="2b954-263">Outra opção para adicionar verbos a um menu em cascata é por meio de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="2b954-263">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="2b954-264">Esse método habilita fontes de dados que fornecem seus comandos de módulo de comando por meio de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esses comandos como verbos em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-264">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="2b954-265">No Windows 7 e posterior, você pode fornecer a mesma implementação de verbo usando [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como você pode com o [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="2b954-265">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="2b954-266">As duas capturas de tela a seguir ilustram o uso de menus em cascata na pasta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="2b954-266">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="2b954-268">A captura de tela a seguir ilustra outra implementação de um menu em cascata na pasta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="2b954-268">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="2b954-270">Como o [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável para uso por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-270">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="2b954-271">Obtendo comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="2b954-271">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="2b954-272">A sintaxe de consulta avançada (AQS) pode expressar uma condição que será avaliada usando as propriedades do item para o qual o verbo está sendo instanciado.</span><span class="sxs-lookup"><span data-stu-id="2b954-272">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="2b954-273">Esse sistema funciona apenas com propriedades rápidas.</span><span class="sxs-lookup"><span data-stu-id="2b954-273">This system works only with fast properties.</span></span> <span data-ttu-id="2b954-274">Essas são propriedades que a fonte de dados do Shell relata como rápido, não retornando [\* \* \* \* SHCOLSTATE \_ lento \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* de [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="2b954-274">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="2b954-275">O Windows 7 e versões posteriores dão suporte a valores canônicos que evitam problemas em compilações localizadas.</span><span class="sxs-lookup"><span data-stu-id="2b954-275">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="2b954-276">A sintaxe canônica a seguir é necessária em compilações localizadas para aproveitar esse aprimoramento do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2b954-276">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="2b954-277">Na seguinte entrada de registro de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2b954-277">In the following example registry entry:</span></span>

-   <span data-ttu-id="2b954-278">O valor **AppliesTo** controla se o verbo é exibido ou oculto.</span><span class="sxs-lookup"><span data-stu-id="2b954-278">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="2b954-279">O valor defaultappliestoto controla qual verbo é o padrão.</span><span class="sxs-lookup"><span data-stu-id="2b954-279">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="2b954-280">O valor HasLUAShield controla se um escudo de controle de conta de usuário (UAC) é exibido.</span><span class="sxs-lookup"><span data-stu-id="2b954-280">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="2b954-281">Neste exemplo, o **valor DefaultAppliesTo** torna esse verbo o padrão para qualquer arquivo com a palavra "exampleText1" em seu nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-281">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="2b954-282">O **valor AppliesTo** habilita o verbo para qualquer arquivo com "exampleText1" no nome.</span><span class="sxs-lookup"><span data-stu-id="2b954-282">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="2b954-283">O **valor HasLUAShield** exibe o blindagem para arquivos com "exampleText2" no nome.</span><span class="sxs-lookup"><span data-stu-id="2b954-283">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="2b954-284">Adicione **a** sub-chave Command e um valor:</span><span class="sxs-lookup"><span data-stu-id="2b954-284">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="2b954-285">No Registro do Windows 7, consulte **Unidade RAIZ de \_ CLASSES \_ HKEY** como um exemplo de \\  verbos do bitlocker que empregam a seguinte abordagem:</span><span class="sxs-lookup"><span data-stu-id="2b954-285">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="2b954-286">AppliesTo = System.Volume.BitlockerProtection:=2</span><span class="sxs-lookup"><span data-stu-id="2b954-286">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="2b954-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True</span><span class="sxs-lookup"><span data-stu-id="2b954-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="2b954-288">Para obter mais informações sobre o AQS, consulte [Sintaxe de consulta avançada.](../search/-search-3x-advancedquerysyntax.md)</span><span class="sxs-lookup"><span data-stu-id="2b954-288">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="2b954-289">Preterido: associando verbos a comandos troca dinâmica de dados dados</span><span class="sxs-lookup"><span data-stu-id="2b954-289">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="2b954-290">A DDE foi preterida; em vez disso, use [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="2b954-290">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="2b954-291">A DDE foi preterida porque depende de uma mensagem de janela de difusão para descobrir o servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="2b954-291">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="2b954-292">Uma trava do servidor DDE para a mensagem da janela de difusão e, portanto, trava as conversas de DDE para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2b954-292">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="2b954-293">É comum que um único aplicativo travado cause travas subsequentes em toda a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b954-293">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="2b954-294">O [**método IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) é mais robusto e tem melhor suporte de ativação porque usa a ativação COM do manipulador.</span><span class="sxs-lookup"><span data-stu-id="2b954-294">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="2b954-295">No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho do buffer encontradas no DDE e [**no CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)</span><span class="sxs-lookup"><span data-stu-id="2b954-295">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="2b954-296">Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)</span><span class="sxs-lookup"><span data-stu-id="2b954-296">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="2b954-297">Isso é mais simples e não perde informações de namespace como ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2b954-297">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="2b954-298">Para obter mais informações sobre [**consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell para atributos de associação de arquivo, consulte [Tipos percebidos e Registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2b954-298">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="2b954-299">Concluindo tarefas de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="2b954-299">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="2b954-300">As tarefas a seguir para implementar verbos são relevantes para as implementações de verbo estáticos e dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="2b954-300">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="2b954-301">Para obter mais informações sobre verbos dinâmicos, consulte [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="2b954-301">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="2b954-302">Personalizando o menu de atalho para objetos shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="2b954-302">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="2b954-303">Muitos objetos de shell predefinidos têm menus de atalho que podem ser personalizados.</span><span class="sxs-lookup"><span data-stu-id="2b954-303">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="2b954-304">Registre o comando praticamente da mesma maneira que você registra tipos de arquivo típicos, mas use o nome do objeto predefinido como o nome do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-304">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="2b954-305">Uma lista de objetos predefinidos está na seção *objetos do Shell predefinidos* da [criação de manipuladores de extensão do Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="2b954-305">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="2b954-306">Esses objetos de shell predefinidos cujos menus de atalho podem ser personalizados com a adição de verbos no registro são marcados na tabela com o verbo do Word.</span><span class="sxs-lookup"><span data-stu-id="2b954-306">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="2b954-307">Estendendo um novo submenu</span><span class="sxs-lookup"><span data-stu-id="2b954-307">Extending a New Submenu</span></span>

<span data-ttu-id="2b954-308">Quando um usuário abre o menu **arquivo** no Windows Explorer, um dos comandos exibidos é **novo**.</span><span class="sxs-lookup"><span data-stu-id="2b954-308">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="2b954-309">A seleção desse comando exibe um submenu.</span><span class="sxs-lookup"><span data-stu-id="2b954-309">Selecting this command displays a submenu.</span></span> <span data-ttu-id="2b954-310">Por padrão, o submenu contém dois comandos, **pasta** e **atalho**, que permitem aos usuários criar subpastas e atalhos.</span><span class="sxs-lookup"><span data-stu-id="2b954-310">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="2b954-311">Esse submenu pode ser estendido para incluir comandos de criação de arquivo para qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-311">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="2b954-312">Para adicionar um comando de criação de arquivo ao **novo** submenu, os arquivos do aplicativo devem ter um tipo de arquivo associado.</span><span class="sxs-lookup"><span data-stu-id="2b954-312">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="2b954-313">Inclua uma subchave **ShellNew** sob o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-313">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="2b954-314">Quando o comando **novo** do menu **arquivo** é selecionado, o Shell adiciona o tipo de arquivo ao **novo** submenu.</span><span class="sxs-lookup"><span data-stu-id="2b954-314">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="2b954-315">A cadeia de caracteres de exibição do comando é a cadeia de caracteres descritiva que é atribuída ao ProgID do programa.</span><span class="sxs-lookup"><span data-stu-id="2b954-315">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="2b954-316">Para especificar o método de criação de arquivo, atribua um ou mais valores de dados à subchave **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="2b954-316">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="2b954-317">Os valores disponíveis são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b954-317">The available values are listed in the following table.</span></span>



| <span data-ttu-id="2b954-318">Valor da subchave ShellNew</span><span class="sxs-lookup"><span data-stu-id="2b954-318">ShellNew subkey value</span></span> | <span data-ttu-id="2b954-319">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b954-319">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b954-320">Comando</span><span class="sxs-lookup"><span data-stu-id="2b954-320">Command</span></span>               | <span data-ttu-id="2b954-321">Executa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b954-321">Executes an application.</span></span> <span data-ttu-id="2b954-322">Esse **valor \_ REG SZ** especifica o caminho do aplicativo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="2b954-322">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="2b954-323">Por exemplo, você pode defini-lo para iniciar um assistente.</span><span class="sxs-lookup"><span data-stu-id="2b954-323">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="2b954-324">Dados</span><span class="sxs-lookup"><span data-stu-id="2b954-324">Data</span></span>                  | <span data-ttu-id="2b954-325">Cria um arquivo que contém dados especificados.</span><span class="sxs-lookup"><span data-stu-id="2b954-325">Creates a file containing specified data.</span></span> <span data-ttu-id="2b954-326">Esse **valor \_ REG BINARY** especifica os dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b954-326">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="2b954-327">**Os** dados serão ignorados se **NullFile** ou **FileName** for especificado.</span><span class="sxs-lookup"><span data-stu-id="2b954-327">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="2b954-328">FileName</span><span class="sxs-lookup"><span data-stu-id="2b954-328">FileName</span></span>              | <span data-ttu-id="2b954-329">Cria um arquivo que é uma cópia de um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2b954-329">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="2b954-330">Esse **valor \_ REG SZ** especifica o caminho totalmente qualificado do arquivo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="2b954-330">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="2b954-331">NullFile</span><span class="sxs-lookup"><span data-stu-id="2b954-331">NullFile</span></span>              | <span data-ttu-id="2b954-332">Cria um arquivo vazio.</span><span class="sxs-lookup"><span data-stu-id="2b954-332">Creates an empty file.</span></span> <span data-ttu-id="2b954-333">**NullFile** não tem um valor atribuído.</span><span class="sxs-lookup"><span data-stu-id="2b954-333">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="2b954-334">Se **NullFile** for especificado, os valores do Registro **Data** e **FileName** serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="2b954-334">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="2b954-335">O exemplo de chave do Registro e a captura de tela a seguir ilustram o submenu **Novo** para o tipo de arquivo .myp-ms.</span><span class="sxs-lookup"><span data-stu-id="2b954-335">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="2b954-336">Ele tem um comando, **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="2b954-336">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="2b954-337">A captura de tela ilustra **o** submenu Novo.</span><span class="sxs-lookup"><span data-stu-id="2b954-337">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="2b954-338">Quando um usuário seleciona **MyProgram Application** no **submenu** **Novo,** o Shell cria um arquivo chamado Novo **MyProgram Application.myp-ms** e o passa paraMyProgram.exe.</span><span class="sxs-lookup"><span data-stu-id="2b954-338">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![captura de tela do Windows Explorer mostrando um novo comando "aplicativo myprogram" no submenu "novo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="2b954-340">Criando manipuladores do "arrastar e soltar"</span><span class="sxs-lookup"><span data-stu-id="2b954-340">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="2b954-341">O procedimento básico para implementar um manipulador do tipo "arrastar e soltar" é o mesmo que para manipuladores de menu de atalho convencionais.</span><span class="sxs-lookup"><span data-stu-id="2b954-341">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="2b954-342">No entanto, os manipuladores de menu de atalho normalmente usam apenas o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passado para o método [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) do manipulador para extrair o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="2b954-342">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="2b954-343">Um manipulador do tipo "arrastar e soltar" pode implementar um manipulador de dados mais sofisticado para modificar o comportamento do objeto arrastado.</span><span class="sxs-lookup"><span data-stu-id="2b954-343">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="2b954-344">Quando um usuário clica com o botão direito do mouse em um objeto Shell para arrastar um objeto, um menu de atalho é exibido quando o usuário tenta descartar o objeto.</span><span class="sxs-lookup"><span data-stu-id="2b954-344">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="2b954-345">A captura de tela a seguir ilustra um menu de atalho típico do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="2b954-345">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![captura de tela do menu de atalho arrastar e soltar](images/context-menu/context-dragdrop.png)

<span data-ttu-id="2b954-347">Um manipulador de arrastar e soltar é um manipulador de menu de atalho que pode adicionar itens a esse menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2b954-347">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="2b954-348">Os manipuladores de arrastar e soltar normalmente são registrados na subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b954-348">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="2b954-349">Adicione uma subchave sob a subchave **DragDropHandlers** chamada para o manipulador de arrastar e soltar e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="2b954-349">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="2b954-350">O exemplo a seguir habilita o manipulador de arrastar e soltar **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="2b954-350">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="2b954-351">Suprimindo verbos e controlando a visibilidade</span><span class="sxs-lookup"><span data-stu-id="2b954-351">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="2b954-352">Você pode usar as configurações da política do Windows para controlar a visibilidade do verbo.</span><span class="sxs-lookup"><span data-stu-id="2b954-352">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="2b954-353">Os verbos podem ser suprimidos por meio de configurações de política adicionando um valor de **SuppressionPolicy** ou um valor de GUID **SuppressionPolicyEx** à subchave do registro do verbo.</span><span class="sxs-lookup"><span data-stu-id="2b954-353">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="2b954-354">Defina o valor da subchave **SuppressionPolicy** para a ID da política.</span><span class="sxs-lookup"><span data-stu-id="2b954-354">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="2b954-355">Se a política for ativada, o verbo e sua entrada de menu de atalho associada serão suprimidos.</span><span class="sxs-lookup"><span data-stu-id="2b954-355">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="2b954-356">Para obter possíveis valores de ID de política, consulte a enumeração de [**restrições**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="2b954-356">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="2b954-357">Empregando o modelo de seleção de verbo</span><span class="sxs-lookup"><span data-stu-id="2b954-357">Employing the Verb Selection Model</span></span>

<span data-ttu-id="2b954-358">Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item.</span><span class="sxs-lookup"><span data-stu-id="2b954-358">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="2b954-359">Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="2b954-359">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="2b954-360">Os valores possíveis para o modelo de seleção de verbo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="2b954-360">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="2b954-361">Especifique o valor de MultiSelectModel para todos os verbos.</span><span class="sxs-lookup"><span data-stu-id="2b954-361">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="2b954-362">Se o valor de MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu.</span><span class="sxs-lookup"><span data-stu-id="2b954-362">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="2b954-363">Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, o **documento** é assumido.</span><span class="sxs-lookup"><span data-stu-id="2b954-363">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="2b954-364">**Especifique** Único para verbos que suportam apenas uma única seleção.</span><span class="sxs-lookup"><span data-stu-id="2b954-364">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="2b954-365">**Especifique** Player para verbos que suportam qualquer número de itens.</span><span class="sxs-lookup"><span data-stu-id="2b954-365">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="2b954-366">**Especifique** Documento para verbos que criam uma janela de nível superior para cada item.</span><span class="sxs-lookup"><span data-stu-id="2b954-366">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="2b954-367">Isso limita o número de itens ativados e ajuda a evitar a falta de recursos do sistema se o usuário abrir muitas janelas.</span><span class="sxs-lookup"><span data-stu-id="2b954-367">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="2b954-368">Quando o número de itens selecionados não corresponder ao modelo de seleção de verbo ou for maior que os limites padrão descritos na tabela a seguir, o verbo não aparecerá.</span><span class="sxs-lookup"><span data-stu-id="2b954-368">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="2b954-369">Tipo de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="2b954-369">Type of verb implementation</span></span> | <span data-ttu-id="2b954-370">Documento</span><span class="sxs-lookup"><span data-stu-id="2b954-370">Document</span></span> | <span data-ttu-id="2b954-371">Jogador</span><span class="sxs-lookup"><span data-stu-id="2b954-371">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="2b954-372">Herdada</span><span class="sxs-lookup"><span data-stu-id="2b954-372">Legacy</span></span>                      | <span data-ttu-id="2b954-373">15 itens</span><span class="sxs-lookup"><span data-stu-id="2b954-373">15 items</span></span> | <span data-ttu-id="2b954-374">100 itens</span><span class="sxs-lookup"><span data-stu-id="2b954-374">100 items</span></span> |
| <span data-ttu-id="2b954-375">COM</span><span class="sxs-lookup"><span data-stu-id="2b954-375">COM</span></span>                         | <span data-ttu-id="2b954-376">15 itens</span><span class="sxs-lookup"><span data-stu-id="2b954-376">15 items</span></span> | <span data-ttu-id="2b954-377">Sem limite</span><span class="sxs-lookup"><span data-stu-id="2b954-377">No limit</span></span>  |



 

<span data-ttu-id="2b954-378">A seguir estão exemplos de entradas do Registro usando o valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="2b954-378">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="2b954-379">Usando atributos de item</span><span class="sxs-lookup"><span data-stu-id="2b954-379">Using Item Attributes</span></span>

<span data-ttu-id="2b954-380">Os [**valores de sinalizador SFGAO**](sfgao.md) dos atributos do Shell para um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2b954-380">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="2b954-381">Para usar esse recurso de atributo, adicione os seguintes valores **REG \_ DWORD** sob o verbo:</span><span class="sxs-lookup"><span data-stu-id="2b954-381">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="2b954-382">O valor AttributeMask especifica o [**valor de SFGAO**](sfgao.md) dos valores de bit da máscara com o que testar.</span><span class="sxs-lookup"><span data-stu-id="2b954-382">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="2b954-383">O valor AttributeValue especifica o [**valor SFGAO**](sfgao.md) dos bits testados.</span><span class="sxs-lookup"><span data-stu-id="2b954-383">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="2b954-384">O ImpliedSelectionModel especifica zero para verbos de item ou diferente de zero para verbos no menu de atalho de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="2b954-384">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="2b954-385">Na entrada de registro de exemplo a seguir, AttributeMask é definido como [**SFGAO \_ READONLY**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="2b954-385">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="2b954-386">Implementando verbos personalizados para pastas por meio de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="2b954-386">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="2b954-387">No Windows 7 e posterior, você pode adicionar verbos a uma pasta por meio de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="2b954-387">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="2b954-388">Para obter mais informações sobre Desktop.ini, [consulte How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="2b954-388">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="2b954-389">Desktop.ini arquivos devem ser sempre marcados como ocultos do **sistema** para que  +   não sejam exibidos aos usuários.</span><span class="sxs-lookup"><span data-stu-id="2b954-389">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="2b954-390">**Para adicionar verbos personalizados para pastas por meio de um arquivo Desktop.ini, execute as seguintes etapas:**</span><span class="sxs-lookup"><span data-stu-id="2b954-390">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="2b954-391">Crie uma pasta que esteja marcada como **somente leitura** ou **sistema**.</span><span class="sxs-lookup"><span data-stu-id="2b954-391">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="2b954-392">Crie um arquivo de Desktop.ini que inclui um \[ . ShellClassInfo \] DirectoryClass = ProgID da pasta.</span><span class="sxs-lookup"><span data-stu-id="2b954-392">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="2b954-393">No registro, crie o ProgID da pasta **\_ \_ raiz das classes hKey** \\  com um valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="2b954-393">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="2b954-394">O valor CanUseForDirectory evita o uso indevido de ProgIDs que estão definidos para não participar da implementação de verbos personalizados para pastas por meio de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="2b954-394">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="2b954-395">Adicione verbos na subchave ProgID da **pasta**, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2b954-395">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="2b954-396">Esses verbos podem ser o verbo padrão; nesse caso, clicar duas vezes na pasta ativa o verbo.</span><span class="sxs-lookup"><span data-stu-id="2b954-396">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b954-397">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b954-397">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b954-398">Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="2b954-398">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="2b954-399">Escolhendo um verbo estático ou dinâmico para o menu de atalho</span><span class="sxs-lookup"><span data-stu-id="2b954-399">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="2b954-400">Personalizando um menu de atalho usando verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="2b954-400">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="2b954-401">Menus de atalho (contexto) e manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="2b954-401">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="2b954-402">Verbos e associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="2b954-402">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="2b954-403">Referência do menu de atalho</span><span class="sxs-lookup"><span data-stu-id="2b954-403">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
