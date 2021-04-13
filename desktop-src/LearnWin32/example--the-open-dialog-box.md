---
title: Exemplo da caixa de diálogo abrir
description: O exemplo de formas que estamos usando é um pouco forçado. Vamos recorrer a um objeto COM que você pode usar em um programa do Windows real na caixa de diálogo abrir.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365979"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="5e48a-104">Exemplo: a caixa de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="5e48a-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="5e48a-105">O `Shapes` exemplo que estamos usando é um pouco forçado.</span><span class="sxs-lookup"><span data-stu-id="5e48a-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="5e48a-106">Vamos recorrer a um objeto COM que você pode usar em um programa do Windows real: a caixa de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="5e48a-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![captura de tela mostrando a caixa de diálogo abrir](images/fileopen01.png)

<span data-ttu-id="5e48a-108">Para mostrar a caixa de diálogo **abrir** , um programa pode usar um objeto com chamado objeto de caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="5e48a-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="5e48a-109">A caixa de diálogo item comum implementa uma interface chamada [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), que é declarada no arquivo de cabeçalho ShObjIdl. h.</span><span class="sxs-lookup"><span data-stu-id="5e48a-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="5e48a-110">Aqui está um programa que exibe a caixa de diálogo **abrir** para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5e48a-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="5e48a-111">Se o usuário selecionar um arquivo, o programa mostrará uma caixa de diálogo que contém o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e48a-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="5e48a-112">Esse código usa alguns conceitos que serão descritos posteriormente no módulo, portanto, não se preocupe se você não entender tudo aqui.</span><span class="sxs-lookup"><span data-stu-id="5e48a-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="5e48a-113">Aqui está uma estrutura de tópicos básica do código:</span><span class="sxs-lookup"><span data-stu-id="5e48a-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="5e48a-114">Chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="5e48a-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="5e48a-115">Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o objeto de caixa de diálogo de item comum e obter um ponteiro para a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e48a-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="5e48a-116">Chame o método **show** do objeto, que mostra a caixa de diálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5e48a-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="5e48a-117">Esse método é bloqueado até que o usuário desperca a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5e48a-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="5e48a-118">Chame o método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e48a-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="5e48a-119">Esse método retorna um ponteiro para um segundo objeto COM, chamado de objeto de *item de shell* .</span><span class="sxs-lookup"><span data-stu-id="5e48a-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="5e48a-120">O item de Shell, que implementa a interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , representa o arquivo selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e48a-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="5e48a-121">Chame o método [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) do item do Shell.</span><span class="sxs-lookup"><span data-stu-id="5e48a-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="5e48a-122">Esse método obtém o caminho do arquivo, na forma de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e48a-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="5e48a-123">Mostrar uma caixa de mensagem que exibe o caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e48a-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="5e48a-124">Chame [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) para cancelar a inicialização da biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="5e48a-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="5e48a-125">As etapas 1, 2 e 7 chamam funções que são definidas pela biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="5e48a-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="5e48a-126">Essas são funções COM genéricas.</span><span class="sxs-lookup"><span data-stu-id="5e48a-126">These are generic COM functions.</span></span> <span data-ttu-id="5e48a-127">Etapas 3 a 5 métodos de chamada que são definidos pelo objeto de caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="5e48a-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="5e48a-128">Este exemplo mostra as duas variedades de criação de objeto: a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) genérica e um método ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) que é específico para o objeto de caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="5e48a-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="5e48a-129">Avançar</span><span class="sxs-lookup"><span data-stu-id="5e48a-129">Next</span></span>

[<span data-ttu-id="5e48a-130">Gerenciando o tempo de vida de um objeto</span><span class="sxs-lookup"><span data-stu-id="5e48a-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="5e48a-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e48a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e48a-132">Exemplo de caixa de diálogo aberta</span><span class="sxs-lookup"><span data-stu-id="5e48a-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 