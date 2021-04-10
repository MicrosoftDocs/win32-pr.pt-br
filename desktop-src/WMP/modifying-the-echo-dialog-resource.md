---
title: Modificando o recurso de diálogo de eco
description: Modificando o recurso de diálogo de eco
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, recurso de caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292491"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="8dfa1-109">Modificando o recurso de diálogo de eco</span><span class="sxs-lookup"><span data-stu-id="8dfa1-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="8dfa1-110">Você precisa alterar o recurso de caixa de diálogo que é a interface do usuário para o objeto da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="8dfa1-111">Você pode primeiro alterar a caixa de edição e o rótulo existentes para que sejam úteis para a propriedade de tempo de atraso e, em seguida, adicionar uma segunda caixa de edição e rótulo para a propriedade de combinação úmida.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="8dfa1-112">Para editar o recurso de caixa de diálogo no Visual C++:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="8dfa1-113">Clique na guia **ResourceView** no espaço de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="8dfa1-114">Expanda a árvore de recursos abrindo a pasta de nível superior.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="8dfa1-115">Abra a pasta **caixa de diálogo** .</span><span class="sxs-lookup"><span data-stu-id="8dfa1-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="8dfa1-116">Clique duas vezes no nome do recurso de caixa de diálogo, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="8dfa1-117">O editor de recursos é exibido no painel direito.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="8dfa1-118">Alterando os recursos existentes</span><span class="sxs-lookup"><span data-stu-id="8dfa1-118">Changing the Existing Resources</span></span>

<span data-ttu-id="8dfa1-119">Para alterar os recursos da página de propriedades existente para a propriedade tempo de atraso:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="8dfa1-120">Primeiro, altere o texto no controle de texto estático existente.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="8dfa1-121">Clique com o botão direito do mouse no controle e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="8dfa1-122">No campo **legenda** , digite a nova legenda:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="8dfa1-123">Feche a caixa de diálogo Propriedades de texto.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="8dfa1-124">Agora, altere o nome do controle caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="8dfa1-125">Para fazer isso, clique com o botão direito do mouse no controle e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="8dfa1-126">No campo **ID** , digite um novo nome para o controle:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="8dfa1-127">Feche a caixa de diálogo Editar propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="8dfa1-128">Salve o recurso.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-128">Save the resource.</span></span>
6.  <span data-ttu-id="8dfa1-129">Responda **Sim** se for solicitado a recarregar o arquivo Resource. h.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="8dfa1-130">Clique na guia **fileview** no espaço de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="8dfa1-131">Abrir Resource. h</span><span class="sxs-lookup"><span data-stu-id="8dfa1-131">Open resource.h</span></span>
8.  <span data-ttu-id="8dfa1-132">Localize o \# recurso definir para a caixa de edição fator de escala (IDC \_ SCALEFACTOR) e exclua-o.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="8dfa1-133">Ele deve ter o mesmo número de ID que o IDC \_ DelayTime.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="8dfa1-134">Adicionando os novos recursos</span><span class="sxs-lookup"><span data-stu-id="8dfa1-134">Adding the New Resources</span></span>

<span data-ttu-id="8dfa1-135">Para adicionar os novos recursos da página de propriedades para a propriedade de combinação úmida:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="8dfa1-136">Clique na guia **ResourceView** no espaço de trabalho do projeto para selecioná-la.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="8dfa1-137">Clique duas vezes no nome da caixa de diálogo página de propriedades, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="8dfa1-138">O editor de recursos é exibido no painel direito.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="8dfa1-139">Use o Toolbox para adicionar um controle de texto estático e uma caixa de edição à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="8dfa1-140">Clique com o botão direito do mouse no controle de texto estático e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="8dfa1-141">Digite um novo nome para o controle de texto estático no campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="8dfa1-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="8dfa1-142">Digite uma legenda para o rótulo:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="8dfa1-143">Feche a caixa de diálogo Propriedades de texto.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="8dfa1-144">Clique com o botão direito do mouse na caixa de edição e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="8dfa1-145">Digite um novo nome para a caixa de edição no campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="8dfa1-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="8dfa1-146">Feche a caixa de diálogo Editar propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="8dfa1-147">Ao salvar o projeto, você pode ser solicitado a recarregar o Resource. h.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="8dfa1-148">Clique em **Sim** se isso acontecer.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="8dfa1-149">A caixa de diálogo Editor de recursos deve adicionar os nomes de recursos e os números de ID a Resource. h para os itens adicionados.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="8dfa1-150">Se, por algum motivo, isso não acontecer, você deverá abrir Resource. h e digitar novas entradas para o controle rótulo e caixa de edição e atribuir cada um número de ID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="8dfa1-151">Modificando e adicionando os recursos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8dfa1-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="8dfa1-152">O código de exemplo do assistente de plug-in especifica um recurso de cadeia de caracteres chamado IDS \_ SCALERANGEERROR que contém uma mensagem a ser exibida quando a entrada do usuário está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="8dfa1-153">Você pode modificar esse recurso para se adequar às suas necessidades pelo valor do tempo de atraso seguindo estas etapas no Visual C++:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="8dfa1-154">Clique na guia **ResourceView** .</span><span class="sxs-lookup"><span data-stu-id="8dfa1-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="8dfa1-155">Abra a pasta da **tabela de cadeia de caracteres** .</span><span class="sxs-lookup"><span data-stu-id="8dfa1-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="8dfa1-156">Clique duas vezes no ícone de **tabela de cadeia de caracteres** para abrir o editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="8dfa1-157">Clique duas vezes no nome do recurso que você deseja editar, nesse caso, IDS \_ SCALERANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="8dfa1-158">A caixa de diálogo Propriedades da cadeia de caracteres é exibida.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="8dfa1-159">Altere o nome no campo **ID** para IDs \_ DELAYRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="8dfa1-160">Altere o texto no campo **legenda** :</span><span class="sxs-lookup"><span data-stu-id="8dfa1-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="8dfa1-161">Feche a caixa de diálogo Propriedades da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="8dfa1-162">Em seguida, adicione um novo recurso de cadeia de caracteres para a mensagem de erro de propriedade de mistura úmida.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="8dfa1-163">Clique duas vezes na linha vazia na parte inferior do editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="8dfa1-164">Altere o nome no campo **ID** para IDs \_ MIXRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="8dfa1-165">Adicione o seguinte texto ao campo de **legenda** :</span><span class="sxs-lookup"><span data-stu-id="8dfa1-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="8dfa1-166">Feche a caixa de diálogo Propriedades da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="8dfa1-167">Há dois outros valores que você deve alterar na tabela de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="8dfa1-168">IDS \_ FriendlyName é o nome que aparece na interface do usuário do Windows Media Player para identificar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="8dfa1-169">\_Descrição de IDs permite que você informe o usuário sobre seu plug-in.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="8dfa1-170">Essas duas cadeias de caracteres são passadas como parâmetros para a função **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , que é chamada no método DllRegisterServer em Echodll. cpp.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dfa1-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dfa1-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dfa1-172">**Modificando a página de propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="8dfa1-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




