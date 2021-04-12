---
title: Adicionando e modificando os eventos
description: Adicionando e modificando os eventos
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292472"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="ef24a-109">Adicionando e modificando os eventos</span><span class="sxs-lookup"><span data-stu-id="ef24a-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="ef24a-110">Você precisa fornecer manipuladores de eventos para os \_ eventos de alteração en que ocorrem quando o usuário altera o texto nas caixas de edição da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef24a-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="ef24a-111">Esses manipuladores de eventos têm uma implementação simples que apenas habilita a **aplicação** na caixa de diálogo página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef24a-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="ef24a-112">Modificando o manipulador de eventos do fator de escala</span><span class="sxs-lookup"><span data-stu-id="ef24a-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="ef24a-113">Você precisa alterar o nome do manipulador de eventos existente que o assistente de plug-in forneceu para a caixa de edição do fator de escala.</span><span class="sxs-lookup"><span data-stu-id="ef24a-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="ef24a-114">Você deve alterar o nome de OnChangeScale para OnChangeDelay em três locais:</span><span class="sxs-lookup"><span data-stu-id="ef24a-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="ef24a-115">Em EchoPropPage. h, altere o nome na seção macro do mapa de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ef24a-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="ef24a-116">Substitua a linha que mapeia o evento de alteração do fator de escala para o método OnChangeScale com o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="ef24a-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="ef24a-117">Em EchoPropPage. h, altere o nome na linha que protótipos da função OnChangeScale:</span><span class="sxs-lookup"><span data-stu-id="ef24a-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="ef24a-118">Em EchoPropPage. cpp, altere o nome no cabeçalho da função:</span><span class="sxs-lookup"><span data-stu-id="ef24a-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="ef24a-119">Adicionando o manipulador de eventos de mixagem úmida</span><span class="sxs-lookup"><span data-stu-id="ef24a-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="ef24a-120">Você pode adicionar facilmente o manipulador de eventos para o \_ evento de alteração en que é anexado ao \_ controle da caixa de edição WETMIX do IDC.</span><span class="sxs-lookup"><span data-stu-id="ef24a-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="ef24a-121">No editor de recursos da caixa de diálogo:</span><span class="sxs-lookup"><span data-stu-id="ef24a-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="ef24a-122">Clique com o botão direito do mouse na \_ caixa de edição IDC WETMIX e escolha **eventos**.</span><span class="sxs-lookup"><span data-stu-id="ef24a-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="ef24a-123">A caixa de diálogo novo manipulador de mensagens e eventos do Windows é exibida.</span><span class="sxs-lookup"><span data-stu-id="ef24a-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="ef24a-124">Na caixa **classe ou objeto a ser manipulada** , clique no nome do recurso da caixa de edição, IDC \_ WETMIX.</span><span class="sxs-lookup"><span data-stu-id="ef24a-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="ef24a-125">Na caixa **novas mensagens/eventos do Windows** , clique em en \_ alterar para selecioná-lo.</span><span class="sxs-lookup"><span data-stu-id="ef24a-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="ef24a-126">Clique em **Adicionar manipulador**.</span><span class="sxs-lookup"><span data-stu-id="ef24a-126">Click **Add Handler**.</span></span> <span data-ttu-id="ef24a-127">A caixa de diálogo Adicionar função de membro é exibida.</span><span class="sxs-lookup"><span data-stu-id="ef24a-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="ef24a-128">Na caixa **nome da função de membro** , digite o nome OnChangeWetmix.</span><span class="sxs-lookup"><span data-stu-id="ef24a-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="ef24a-129">Clique em **OK** para fechar a caixa de diálogo Adicionar função de membro.</span><span class="sxs-lookup"><span data-stu-id="ef24a-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="ef24a-130">Clique em **OK** para retornar para o editor de recursos da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ef24a-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="ef24a-131">Visual C++ adiciona automaticamente o código para o mapa de mensagens e para a função de manipulador de eventos para EchoPropPage. h.</span><span class="sxs-lookup"><span data-stu-id="ef24a-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="ef24a-132">O código que ele insere fornece um comentário TODO, no qual você pode adicionar a implementação no cabeçalho da função.</span><span class="sxs-lookup"><span data-stu-id="ef24a-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="ef24a-133">Esse é um estilo um pouco diferente do que o código de exemplo do assistente de plug-in do Windows Media Player usa, mas é aceitável.</span><span class="sxs-lookup"><span data-stu-id="ef24a-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="ef24a-134">Se você deseja escrever sua implementação no arquivo de cabeçalho ou movê-lo para EchoPropPage. cpp, você precisa.</span><span class="sxs-lookup"><span data-stu-id="ef24a-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="ef24a-135">Em ambos os casos, a implementação precisa apenas de uma única linha de código adicional para habilitar a **aplicação** na caixa de diálogo da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef24a-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="ef24a-136">Insira esta linha de código antes da linha que retorna da função:</span><span class="sxs-lookup"><span data-stu-id="ef24a-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="ef24a-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef24a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef24a-138">**Modificando a página de propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="ef24a-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




