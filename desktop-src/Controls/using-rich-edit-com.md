---
title: Como usar OLE em controles de edição Rich
description: Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104084413"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="437f6-103">Como usar OLE em controles de edição Rich</span><span class="sxs-lookup"><span data-stu-id="437f6-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="437f6-104">Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="437f6-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="437f6-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="437f6-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="437f6-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="437f6-106">Technologies</span></span>

-   [<span data-ttu-id="437f6-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="437f6-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="437f6-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="437f6-108">Prerequisites</span></span>

-   <span data-ttu-id="437f6-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="437f6-109">C/C++</span></span>
-   <span data-ttu-id="437f6-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="437f6-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="437f6-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="437f6-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="437f6-112">Usar uma interface de edição rica</span><span class="sxs-lookup"><span data-stu-id="437f6-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="437f6-113">Os controles de edição avançados expõem algumas de suas funcionalidades por meio de interfaces de Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="437f6-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="437f6-114">Ao obter uma interface de um controle, você obtém a capacidade de trabalhar com outros objetos dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="437f6-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="437f6-115">Você pode obter essa interface enviando a mensagem [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="437f6-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="437f6-116">Na interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) , você pode obter interfaces usadas no [modelo de objeto de texto](text-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="437f6-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="437f6-117">Outra interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), é implementada por aplicativos para definir o comportamento do controle quando ele interage com objetos.</span><span class="sxs-lookup"><span data-stu-id="437f6-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="437f6-118">Inserir um objeto em um controle de edição rico</span><span class="sxs-lookup"><span data-stu-id="437f6-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="437f6-119">O exemplo de código a seguir insere um objeto File em um controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="437f6-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="437f6-120">Se um programa estiver associado ao tipo de arquivo no computador do usuário (por exemplo, o Microsoft Excel para um arquivo. xls), o conteúdo do arquivo será exibido no controle; caso contrário, um ícone será exibido.</span><span class="sxs-lookup"><span data-stu-id="437f6-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="437f6-121">Obtenha a interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="437f6-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="437f6-122">Crie um armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="437f6-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="437f6-123">Configure o formato de dados.</span><span class="sxs-lookup"><span data-stu-id="437f6-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="437f6-124">Obtenha um ponteiro para o site de exibição.</span><span class="sxs-lookup"><span data-stu-id="437f6-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="437f6-125">Crie o objeto e recupere sua interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="437f6-125">Create the object and retrieve its **IUnknown** interface.</span></span>

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  <span data-ttu-id="437f6-126">Obtenha a interface IOleObject para o objeto.</span><span class="sxs-lookup"><span data-stu-id="437f6-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="437f6-127">Para garantir que as referências sejam contadas corretamente, notifique o objeto que ele está contido.</span><span class="sxs-lookup"><span data-stu-id="437f6-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="437f6-128">Configurar informações do objeto.</span><span class="sxs-lookup"><span data-stu-id="437f6-128">Set up object info.</span></span>

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  <span data-ttu-id="437f6-129">Mover o cursor para o fim do texto e adicionar um retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="437f6-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="437f6-130">Insira o objeto.</span><span class="sxs-lookup"><span data-stu-id="437f6-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="437f6-131">Limpar.</span><span class="sxs-lookup"><span data-stu-id="437f6-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="437f6-132">Usando IRichEditOleCallback</span><span class="sxs-lookup"><span data-stu-id="437f6-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="437f6-133">Os aplicativos implementam a interface [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) para responder a consultas ou ações relacionadas a OLE que são executadas por um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="437f6-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="437f6-134">Você associa a implementação da interface ao controle enviando uma mensagem em [**\_ SETOLECALLBACK**](em-setolecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="437f6-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="437f6-135">O controle então chama métodos em sua implementação da interface, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="437f6-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="437f6-136">Por exemplo, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) é chamado quando o usuário tenta arrastar ou colar um objeto no controle.</span><span class="sxs-lookup"><span data-stu-id="437f6-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="437f6-137">Se seu aplicativo puder aceitar os dados, sua implementação do método retornará S \_ OK; caso contrário, ele retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="437f6-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="437f6-138">O método também pode executar alguma outra ação, como aviso o usuário de que os arquivos desse tipo não podem ser colocados no controle.</span><span class="sxs-lookup"><span data-stu-id="437f6-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="437f6-139">Função de exemplo InsertObject completa</span><span class="sxs-lookup"><span data-stu-id="437f6-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="437f6-140">O exemplo de código a seguir demonstra os trechos de código anteriores combinados em uma função completa que inclui o tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="437f6-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="437f6-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="437f6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="437f6-142">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="437f6-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="437f6-143">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="437f6-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




