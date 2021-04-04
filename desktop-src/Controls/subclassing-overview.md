---
title: Controles de subclasses
description: Se um controle faz quase tudo que você deseja, mas você precisa de mais alguns recursos, você pode alterar ou adicionar recursos ao controle original por meio de uma subclasse.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008464"
---
# <a name="subclassing-controls"></a><span data-ttu-id="83f88-103">Controles de subclasses</span><span class="sxs-lookup"><span data-stu-id="83f88-103">Subclassing Controls</span></span>

<span data-ttu-id="83f88-104">Se um controle faz quase tudo que você deseja, mas você precisa de mais alguns recursos, você pode alterar ou adicionar recursos ao controle original por meio de uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="83f88-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="83f88-105">Uma subclasse pode ter todos os recursos de uma classe existente, bem como quaisquer recursos adicionais que você queira dar a ela.</span><span class="sxs-lookup"><span data-stu-id="83f88-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="83f88-106">Este documento discute como as subclasses são criadas e inclui os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="83f88-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="83f88-107">Controles de subclasse antes do ComCtl32.dll versão 6</span><span class="sxs-lookup"><span data-stu-id="83f88-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="83f88-108">Armazenando dados do usuário</span><span class="sxs-lookup"><span data-stu-id="83f88-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="83f88-109">Desvantagens da antiga abordagem de subclasse</span><span class="sxs-lookup"><span data-stu-id="83f88-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="83f88-110">Controles de subclasses usando ComCtl32.dll versão 6</span><span class="sxs-lookup"><span data-stu-id="83f88-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="83f88-111">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="83f88-112">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="83f88-113">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="83f88-114">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="83f88-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="83f88-115">Controles de subclasse antes do ComCtl32.dll versão 6</span><span class="sxs-lookup"><span data-stu-id="83f88-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="83f88-116">Você pode colocar um controle em uma subclasse e armazenar dados de usuário em um controle.</span><span class="sxs-lookup"><span data-stu-id="83f88-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="83f88-117">Você faz isso ao usar versões do ComCtl32.dll anteriores à versão 6.</span><span class="sxs-lookup"><span data-stu-id="83f88-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="83f88-118">Há algumas desvantagens na criação de subclasses com versões anteriores do ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="83f88-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="83f88-119">Para criar um novo controle, é melhor começar com um dos controles comuns do Windows e estendê-lo para se adequar a uma necessidade específica.</span><span class="sxs-lookup"><span data-stu-id="83f88-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="83f88-120">Para estender um controle, crie um controle e substitua seu procedimento de janela existente por um novo.</span><span class="sxs-lookup"><span data-stu-id="83f88-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="83f88-121">O novo procedimento intercepta as mensagens do controle e as atua ou transmite-as para o procedimento original para o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="83f88-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="83f88-122">Use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) para substituir o WndProc do controle.</span><span class="sxs-lookup"><span data-stu-id="83f88-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="83f88-123">O exemplo de código a seguir mostra como substituir um WNDPROC.</span><span class="sxs-lookup"><span data-stu-id="83f88-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="83f88-124">Armazenando dados do usuário</span><span class="sxs-lookup"><span data-stu-id="83f88-124">Storing User Data</span></span>

<span data-ttu-id="83f88-125">Talvez você queira armazenar os dados do usuário com uma janela individual.</span><span class="sxs-lookup"><span data-stu-id="83f88-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="83f88-126">Esses dados podem ser usados pelo novo procedimento de janela para determinar como desenhar o controle ou para onde enviar determinadas mensagens.</span><span class="sxs-lookup"><span data-stu-id="83f88-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="83f88-127">Por exemplo, você pode usar dados para armazenar um ponteiro de classe C++ para a classe que representa o controle.</span><span class="sxs-lookup"><span data-stu-id="83f88-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="83f88-128">O exemplo de código a seguir mostra como usar [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) para armazenar dados com uma janela.</span><span class="sxs-lookup"><span data-stu-id="83f88-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="83f88-129">Desvantagens da antiga abordagem de subclasse</span><span class="sxs-lookup"><span data-stu-id="83f88-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="83f88-130">A lista a seguir destaca algumas das desvantagens de usar a abordagem descrita anteriormente para subclasse de um controle.</span><span class="sxs-lookup"><span data-stu-id="83f88-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="83f88-131">O procedimento de janela só pode ser substituído uma vez.</span><span class="sxs-lookup"><span data-stu-id="83f88-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="83f88-132">É difícil remover uma subclasse após sua criação.</span><span class="sxs-lookup"><span data-stu-id="83f88-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="83f88-133">A associação de dados privados a uma janela é ineficiente.</span><span class="sxs-lookup"><span data-stu-id="83f88-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="83f88-134">Para chamar o próximo procedimento em uma cadeia de subclasse, você não pode converter o antigo procedimento de janela e chamá-lo, você deve chamá-lo usando a função [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="83f88-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="83f88-135">Controles de subclasses usando ComCtl32.dll versão 6</span><span class="sxs-lookup"><span data-stu-id="83f88-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="83f88-136">ComCtl32.dll versão 6 é apenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="83f88-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="83f88-137">Os controles comuns com suporte pelo ComCtl32.dll versão 6 não devem ser subclasses (ou superclasses) com procedimentos de janela ANSI.</span><span class="sxs-lookup"><span data-stu-id="83f88-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="83f88-138">O ComCtl32.dll versão 6 contém quatro funções que facilitam a criação de subclasses e eliminam as desvantagens discutidas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="83f88-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="83f88-139">As novas funções encapsulam o gerenciamento envolvido com vários conjuntos de dados de referência, portanto, o desenvolvedor pode se concentrar em recursos de programação e não no gerenciamento de subclasses.</span><span class="sxs-lookup"><span data-stu-id="83f88-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="83f88-140">As funções de subclasse são:</span><span class="sxs-lookup"><span data-stu-id="83f88-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="83f88-141">**SetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="83f88-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="83f88-142">**GetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="83f88-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="83f88-143">**RemoveWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="83f88-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="83f88-144">**DefSubclassProc**</span><span class="sxs-lookup"><span data-stu-id="83f88-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="83f88-145">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-145">SetWindowSubclass</span></span>

<span data-ttu-id="83f88-146">Essa função é usada para inicialmente subclasse de uma janela.</span><span class="sxs-lookup"><span data-stu-id="83f88-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="83f88-147">Cada subclasse é identificada exclusivamente pelo endereço do *pfnSubclass* e seu *uIdSubclass*.</span><span class="sxs-lookup"><span data-stu-id="83f88-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="83f88-148">Ambos são parâmetros da função [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="83f88-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="83f88-149">Várias subclasses podem compartilhar o mesmo procedimento de subclasse e a ID pode identificar cada chamada.</span><span class="sxs-lookup"><span data-stu-id="83f88-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="83f88-150">Para alterar os dados de referência, você pode fazer chamadas subsequentes para **SetWindowSubclass**.</span><span class="sxs-lookup"><span data-stu-id="83f88-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="83f88-151">A vantagem importante é que cada instância de subclasse tem seus próprios dados de referência.</span><span class="sxs-lookup"><span data-stu-id="83f88-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="83f88-152">A declaração de um procedimento de subclasse é ligeiramente diferente de um procedimento de janela regular porque ele tem duas partes adicionais de dados: a ID da subclasse e os dados de referência.</span><span class="sxs-lookup"><span data-stu-id="83f88-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="83f88-153">Os dois últimos parâmetros da declaração de função a seguir mostram isso.</span><span class="sxs-lookup"><span data-stu-id="83f88-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="83f88-154">Toda vez que uma mensagem é recebida pelo novo procedimento de janela, uma ID de subclasse e dados de referência são incluídos.</span><span class="sxs-lookup"><span data-stu-id="83f88-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="83f88-155">Todas as cadeias de caracteres passadas para o procedimento são cadeias de caracteres Unicode, mesmo se o Unicode não for especificado como uma definição de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="83f88-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="83f88-156">O exemplo a seguir mostra uma implementação de esqueleto de um procedimento de janela para um controle de subclasse.</span><span class="sxs-lookup"><span data-stu-id="83f88-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="83f88-157">O procedimento de janela pode ser anexado ao controle no manipulador [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) do procedimento da caixa de diálogo, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="83f88-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="83f88-158">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-158">GetWindowSubclass</span></span>

<span data-ttu-id="83f88-159">Essa função recupera informações sobre uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="83f88-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="83f88-160">Por exemplo, você pode usar [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) para acessar os dados de referência.</span><span class="sxs-lookup"><span data-stu-id="83f88-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="83f88-161">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="83f88-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="83f88-162">Essa função remove as subclasses.</span><span class="sxs-lookup"><span data-stu-id="83f88-162">This function removes subclasses.</span></span> <span data-ttu-id="83f88-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) em combinação com o [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) permite adicionar e remover subclasses dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="83f88-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="83f88-164">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="83f88-164">DefSubclassProc</span></span>

<span data-ttu-id="83f88-165">A função [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) chama o próximo manipulador na cadeia de subclasse.</span><span class="sxs-lookup"><span data-stu-id="83f88-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="83f88-166">A função também recupera a ID e os dados de referência apropriados e passa as informações para o próximo procedimento da janela.</span><span class="sxs-lookup"><span data-stu-id="83f88-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 