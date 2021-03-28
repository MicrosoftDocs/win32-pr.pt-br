---
description: O IContextMenu é a mais potente, mas também a interface mais complicada de implementar.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Como implementar a interface IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921672"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="a0773-103">Como implementar a interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a0773-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="a0773-104">O [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é a mais potente, mas também a interface mais complicada de implementar.</span><span class="sxs-lookup"><span data-stu-id="a0773-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="a0773-105">É altamente recomendável que você implemente um verbo usando um dos métodos de verbo estáticos.</span><span class="sxs-lookup"><span data-stu-id="a0773-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="a0773-106">Para obter mais informações, consulte [escolhendo um método de menu de atalho estático ou dinâmico](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0773-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="a0773-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tem três métodos, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que são discutidos aqui em detalhes.</span><span class="sxs-lookup"><span data-stu-id="a0773-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a0773-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a0773-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a0773-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a0773-109">Technologies</span></span>

-   <span data-ttu-id="a0773-110">C++</span><span class="sxs-lookup"><span data-stu-id="a0773-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a0773-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a0773-111">Prerequisites</span></span>

-   <span data-ttu-id="a0773-112">Verbo estático</span><span class="sxs-lookup"><span data-stu-id="a0773-112">Static Verb</span></span>
-   <span data-ttu-id="a0773-113">Menu de atalho</span><span class="sxs-lookup"><span data-stu-id="a0773-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="a0773-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="a0773-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="a0773-115">Método IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="a0773-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="a0773-116">O método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) do manipulador é usado para retornar o nome canônico de um verbo.</span><span class="sxs-lookup"><span data-stu-id="a0773-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="a0773-117">Esse método é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0773-117">This method is optional.</span></span> <span data-ttu-id="a0773-118">No Windows XP e em versões anteriores do Windows, quando o Windows Explorer tem uma barra de status, esse método é usado para recuperar o texto de ajuda que é exibido na barra de status de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="a0773-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="a0773-119">O parâmetro *idCmd* contém o deslocamento do identificador do comando que foi definido quando [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="a0773-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="a0773-120">Se uma cadeia de caracteres de ajuda for solicitada, *uFlags* será definido como **GCS \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="a0773-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="a0773-121">Copie a cadeia de caracteres de ajuda para o buffer *pszName* , convertê-lo em um **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="a0773-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="a0773-122">A cadeia de caracteres de verbo é solicitada definindo *uFlags* para **GCS \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="a0773-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="a0773-123">Copie a cadeia de caracteres apropriada para *pszName*, assim como com a cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a0773-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="a0773-124">Os sinalizadores do **\_ VALIDATEW** de **\_ validação de GCS** e GCS não são usados pelos manipuladores de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="a0773-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="a0773-125">O exemplo a seguir mostra uma implementação simples de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde ao exemplo de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornecido na seção do [método IContextMenu:: QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) deste tópico.</span><span class="sxs-lookup"><span data-stu-id="a0773-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="a0773-126">Como o manipulador adiciona apenas um item de menu, há apenas um conjunto de cadeias de caracteres que podem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="a0773-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="a0773-127">O método testa se *idCmd* é válido e, se for, retorna a cadeia de caracteres solicitada.</span><span class="sxs-lookup"><span data-stu-id="a0773-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="a0773-128">A função [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) é usada para copiar a cadeia de caracteres solicitada para *pszName* para garantir que a cadeia de caracteres copiada não exceda o tamanho do buffer especificado por *cchName*.</span><span class="sxs-lookup"><span data-stu-id="a0773-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="a0773-129">Este exemplo implementa o suporte somente para os valores Unicode de *uFlags*, pois apenas aqueles foram usados no Windows Explorer desde o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a0773-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="a0773-130">Método IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="a0773-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="a0773-131">Esse método é chamado quando um usuário clica em um item de menu para instruir o manipulador a executar o comando associado.</span><span class="sxs-lookup"><span data-stu-id="a0773-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="a0773-132">O parâmetro *Pici* aponta para uma estrutura que contém as informações necessárias para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="a0773-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="a0773-133">Embora *Pici* seja declarado em shlobj. h como uma estrutura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , na prática geralmente aponta para uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="a0773-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="a0773-134">Essa estrutura é uma versão estendida do **CMINVOKECOMMANDINFO** e tem vários membros adicionais que possibilitam a passagem de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0773-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="a0773-135">Verifique o membro **cbSize** de *Pici* para determinar qual estrutura foi passada.</span><span class="sxs-lookup"><span data-stu-id="a0773-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="a0773-136">Se for uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e o membro **fMask** tiver o sinalizador **\_ \_ Unicode de máscara CMIC** definido, converta *Pici* para **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="a0773-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="a0773-137">Isso permite que seu aplicativo use as informações de Unicode contidas nos últimos cinco membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a0773-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="a0773-138">O membro **lpVerb** ou **lpVerbW** da estrutura é usado para identificar o comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="a0773-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="a0773-139">Os comandos são identificados de uma das duas maneiras a seguir:</span><span class="sxs-lookup"><span data-stu-id="a0773-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="a0773-140">Pela cadeia de caracteres de verbo do comando</span><span class="sxs-lookup"><span data-stu-id="a0773-140">By the command's verb string</span></span>
-   <span data-ttu-id="a0773-141">Pelo deslocamento do identificador do comando</span><span class="sxs-lookup"><span data-stu-id="a0773-141">By the command's identifier offset</span></span>

<span data-ttu-id="a0773-142">Para distinguir entre esses dois casos, verifique a palavra de ordem superior de **lpVerb** para o caso ANSI ou **lpVerbW** para o caso Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0773-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="a0773-143">Se a palavra de ordem superior for diferente de zero, **lpVerb** ou **lpVerbW** manterá uma cadeia de caracteres de verbo.</span><span class="sxs-lookup"><span data-stu-id="a0773-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="a0773-144">Se a palavra de ordem superior for zero, o deslocamento de comando estará na palavra de ordem inferior de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="a0773-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="a0773-145">O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde aos exemplos de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fornecidos antes e depois desta seção.</span><span class="sxs-lookup"><span data-stu-id="a0773-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="a0773-146">O método determina primeiro qual estrutura está sendo passada.</span><span class="sxs-lookup"><span data-stu-id="a0773-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="a0773-147">Em seguida, ele determina se o comando é identificado por seu deslocamento ou seu verbo.</span><span class="sxs-lookup"><span data-stu-id="a0773-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="a0773-148">Se **lpVerb** ou **lpVerbW** mantiver um verbo ou um deslocamento válido, o método exibirá uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a0773-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="a0773-149">Método IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="a0773-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="a0773-150">O Shell chama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar o manipulador de menu de atalho para adicionar seus itens de menu ao menu.</span><span class="sxs-lookup"><span data-stu-id="a0773-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="a0773-151">Ele passa o identificador **HMENU** no parâmetro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="a0773-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="a0773-152">O parâmetro *indexMenu* é definido como o índice a ser usado para o primeiro item de menu a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="a0773-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="a0773-153">Todos os itens de menu que são adicionados pelo manipulador devem ter identificadores que se enquadram entre os valores nos parâmetros *idCmdFirst* e *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="a0773-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="a0773-154">Normalmente, o primeiro identificador de comando é definido como *idCmdFirst*, que é incrementado em um (1) para cada comando adicional.</span><span class="sxs-lookup"><span data-stu-id="a0773-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="a0773-155">Essa prática ajuda a evitar exceder o *idCmdLast* e maximiza o número de identificadores disponíveis caso o Shell chame mais de um manipulador.</span><span class="sxs-lookup"><span data-stu-id="a0773-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="a0773-156">Um *deslocamento de comando* do identificador de item é a diferença entre o identificador e o valor em *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="a0773-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="a0773-157">Armazene o deslocamento de cada item que seu manipulador adiciona ao menu de atalho, pois o Shell poderá usar o deslocamento para identificar o item se ele posteriormente chamar [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="a0773-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="a0773-158">Você também deve atribuir um [verbo](launch.md) a cada comando que você adicionar.</span><span class="sxs-lookup"><span data-stu-id="a0773-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="a0773-159">Um verbo é uma cadeia de caracteres que pode ser usada em vez do deslocamento para identificar o comando quando [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado.</span><span class="sxs-lookup"><span data-stu-id="a0773-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="a0773-160">Ele também é usado por funções como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar comandos de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="a0773-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="a0773-161">Há três sinalizadores que podem ser passados por meio do parâmetro *uFlags* que são relevantes para manipuladores de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="a0773-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="a0773-162">Eles são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0773-162">They are described in the following table.</span></span>



| <span data-ttu-id="a0773-163">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="a0773-163">Flag</span></span>             | <span data-ttu-id="a0773-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0773-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0773-165">\_somente CMF</span><span class="sxs-lookup"><span data-stu-id="a0773-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="a0773-166">O usuário selecionou o comando padrão, normalmente clicando duas vezes no objeto.</span><span class="sxs-lookup"><span data-stu-id="a0773-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="a0773-167">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve retornar o controle para o shell sem modificar o menu.</span><span class="sxs-lookup"><span data-stu-id="a0773-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="a0773-168">CMF \_ padrão</span><span class="sxs-lookup"><span data-stu-id="a0773-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="a0773-169">Nenhum item no menu deve ser o item padrão.</span><span class="sxs-lookup"><span data-stu-id="a0773-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="a0773-170">O método deve adicionar seus comandos ao menu.</span><span class="sxs-lookup"><span data-stu-id="a0773-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="a0773-171">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0773-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="a0773-172">O menu de atalho será exibido normalmente.</span><span class="sxs-lookup"><span data-stu-id="a0773-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="a0773-173">O método deve adicionar seus comandos ao menu.</span><span class="sxs-lookup"><span data-stu-id="a0773-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="a0773-174">Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para adicionar itens de menu à lista.</span><span class="sxs-lookup"><span data-stu-id="a0773-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="a0773-175">Em seguida, retorne um valor **HRESULT** com a severidade definida como êxito de severidade \_ .</span><span class="sxs-lookup"><span data-stu-id="a0773-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="a0773-176">Defina o valor do código para o deslocamento do maior identificador de comando que foi atribuído, além de um (1).</span><span class="sxs-lookup"><span data-stu-id="a0773-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="a0773-177">Por exemplo, suponha que *idCmdFirst* seja definido como 5 e você adicione três itens ao menu com identificadores de comando de 5, 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="a0773-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="a0773-178">O valor de retorno deve ser MAKE \_ HRESULT ( \_ êxito de severidade, 0, 8 + 1).</span><span class="sxs-lookup"><span data-stu-id="a0773-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="a0773-179">O exemplo a seguir mostra uma implementação simples de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que insere um único comando.</span><span class="sxs-lookup"><span data-stu-id="a0773-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="a0773-180">O deslocamento do identificador para o comando é \_ tela de IDM, que é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a0773-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="a0773-181">As variáveis **m \_ pszVerb** e **m \_ pwszVerb** são variáveis privadas que são usadas para armazenar a cadeia de caracteres de verbo independente de idioma associada nos formatos ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0773-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="a0773-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0773-182">Remarks</span></span>

<span data-ttu-id="a0773-183">Para outras tarefas de implementação de verbo, consulte [criando manipuladores de menu de atalho](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a0773-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
