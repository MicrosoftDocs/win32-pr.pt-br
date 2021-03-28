---
description: Quando o usuário clica com o botão direito do mouse em um membro de um tipo de arquivo para exibir a folha de propriedades Propriedades, o Shell chama os manipuladores de folha de propriedades que são registrados para o tipo de arquivo. Cada manipulador pode adicionar uma página personalizada à folha de propriedades padrão.
title: Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988979"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="35c28-104">Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="35c28-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="35c28-105">Quando o usuário clica com o botão direito do mouse em um membro de um tipo de arquivo para exibir a folha de propriedades Propriedades, o Shell chama os manipuladores de folha de propriedades que são registrados para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="35c28-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="35c28-106">Cada manipulador pode adicionar uma página personalizada à folha de propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="35c28-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="35c28-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="35c28-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="35c28-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="35c28-108">Technologies</span></span>

-   <span data-ttu-id="35c28-109">Shell</span><span class="sxs-lookup"><span data-stu-id="35c28-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="35c28-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="35c28-110">Prerequisites</span></span>

-   <span data-ttu-id="35c28-111">Uma compreensão dos menus de atalho</span><span class="sxs-lookup"><span data-stu-id="35c28-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="35c28-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="35c28-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="35c28-113">Etapa 1: registrar um manipulador de folha de propriedades para um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="35c28-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="35c28-114">Além do registro COM (normal Component Object Model), adicione uma subchave **PropertySheetHandlers** à subchave **shellex** da chave ProgID do aplicativo associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="35c28-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="35c28-115">Crie uma subchave de **PropertySheetHandlers** com o nome do manipulador e defina o valor padrão como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador de folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="35c28-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="35c28-116">Para adicionar mais de uma página à folha de propriedades, registre um manipulador para cada página.</span><span class="sxs-lookup"><span data-stu-id="35c28-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="35c28-117">O número máximo de páginas às quais uma folha de propriedades pode dar suporte é 32.</span><span class="sxs-lookup"><span data-stu-id="35c28-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="35c28-118">Para registrar vários manipuladores, crie uma chave na chave **shellex** para cada manipulador, com o valor padrão definido como o GUID CLSID do manipulador.</span><span class="sxs-lookup"><span data-stu-id="35c28-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="35c28-119">Não é necessário criar um objeto distinto para cada manipulador, o que significa que vários manipuladores podem ter o mesmo valor de GUID.</span><span class="sxs-lookup"><span data-stu-id="35c28-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="35c28-120">As páginas serão exibidas na ordem em que suas chaves estão listadas em **shellex**.</span><span class="sxs-lookup"><span data-stu-id="35c28-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="35c28-121">O exemplo a seguir ilustra uma entrada de registro que habilita dois manipuladores de extensão de folha de propriedades para um tipo de arquivo. MYP de exemplo.</span><span class="sxs-lookup"><span data-stu-id="35c28-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="35c28-122">Neste exemplo, um objeto separado é usado para cada página, mas um único objeto também pode ser usado para ambos.</span><span class="sxs-lookup"><span data-stu-id="35c28-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="35c28-123">Etapa 2: Implementando um manipulador de folha de propriedades para um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="35c28-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="35c28-124">Além da implementação geral discutida em [como funcionam os manipuladores de folha de propriedades](propsheet-handlers.md), um manipulador de folha de propriedades para um tipo de arquivo também deve ter uma implementação apropriada da interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="35c28-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="35c28-125">Somente o método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) precisa de uma implementação de não token.</span><span class="sxs-lookup"><span data-stu-id="35c28-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="35c28-126">O shell não chama [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span><span class="sxs-lookup"><span data-stu-id="35c28-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="35c28-127">O método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permite que um manipulador de folha de propriedades adicione uma página a uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="35c28-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="35c28-128">O método tem dois parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="35c28-128">The method has two input parameters.</span></span> <span data-ttu-id="35c28-129">O primeiro, *lpfnAddPage*, é um ponteiro para uma função de retorno de chamada [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) que é usada para fornecer ao shell as informações necessárias para adicionar a página à folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="35c28-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="35c28-130">O segundo, *lParam*, é um valor definido por shell que não é processado pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="35c28-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="35c28-131">Ele é simplesmente passado de volta para o shell quando a função de retorno de chamada é chamada.</span><span class="sxs-lookup"><span data-stu-id="35c28-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="35c28-132">O procedimento geral para implementar [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="35c28-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="35c28-133">**Implementando o método AddPages**</span><span class="sxs-lookup"><span data-stu-id="35c28-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="35c28-134">Atribua valores apropriados aos membros de uma estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="35c28-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="35c28-135">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="35c28-135">In particular:</span></span>
    -   <span data-ttu-id="35c28-136">Atribua a variável que mantém a contagem de referência do manipulador ao membro **pcRefParent** .</span><span class="sxs-lookup"><span data-stu-id="35c28-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="35c28-137">Essa prática impede que o objeto do manipulador seja descarregado enquanto a folha de propriedades ainda está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="35c28-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="35c28-138">Você também pode implementar uma função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) e atribuir seu ponteiro a um membro **pfnCallback** .</span><span class="sxs-lookup"><span data-stu-id="35c28-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="35c28-139">Essa função é chamada quando a página é criada e quando está prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="35c28-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="35c28-140">Crie o identificador HPAGE da página passando a estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) para a função [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="35c28-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="35c28-141">Chame a função que é apontada por *lpfnAddPage*.</span><span class="sxs-lookup"><span data-stu-id="35c28-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="35c28-142">Defina seu primeiro parâmetro para o identificador HPAGE que foi criado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="35c28-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="35c28-143">Defina seu segundo parâmetro para o valor de *lParam* que foi passado para [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) pelo shell.</span><span class="sxs-lookup"><span data-stu-id="35c28-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="35c28-144">Todas as mensagens associadas à página serão passadas para o procedimento da caixa de diálogo que foi atribuído ao membro **pfnDlgProc** da estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="35c28-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="35c28-145">Se você atribuiu uma função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, ela será chamada quando a página estiver prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="35c28-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="35c28-146">Em seguida, seu manipulador pode executar todas as operações de limpeza necessárias, como liberar todas as referências que ela contém.</span><span class="sxs-lookup"><span data-stu-id="35c28-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="35c28-147">O exemplo de código a seguir ilustra uma implementação simples de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .</span><span class="sxs-lookup"><span data-stu-id="35c28-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="35c28-148">A variável **g \_ hinst** é o identificador de instância para a dll e IDD \_ PAGEDLG é a ID de recurso do modelo de caixa de diálogo da página.</span><span class="sxs-lookup"><span data-stu-id="35c28-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="35c28-149">A função **PageDlgProc** é o procedimento da caixa de diálogo que manipula as mensagens da página.</span><span class="sxs-lookup"><span data-stu-id="35c28-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="35c28-150">A variável **g \_ DllRefCount** contém a contagem de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="35c28-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="35c28-151">O método [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) chama [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar a contagem.</span><span class="sxs-lookup"><span data-stu-id="35c28-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="35c28-152">No entanto, a contagem de referência é liberada pela função de retorno de chamada, **PageCallbackProc**, quando a página está prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="35c28-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c28-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="35c28-153">Remarks</span></span>

<span data-ttu-id="35c28-154">Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="35c28-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35c28-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35c28-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c28-156">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="35c28-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
