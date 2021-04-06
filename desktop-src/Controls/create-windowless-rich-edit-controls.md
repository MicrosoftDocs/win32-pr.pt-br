---
title: Como fornecer controles de edição avançados sem janelas com a funcionalidade de janela
description: A funcionalidade de janela inclui a capacidade de receber mensagens e a propriedade de um contexto de dispositivo no qual desenhar. Controles de edição avançados sem janela recebem essa funcionalidade por meio de um par de interfaces ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103917085"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="b55e3-104">Como fornecer controles de edição avançados sem janelas com a funcionalidade de janela</span><span class="sxs-lookup"><span data-stu-id="b55e3-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="b55e3-105">A funcionalidade de janela inclui a capacidade de receber mensagens e a propriedade de um contexto de dispositivo no qual desenhar.</span><span class="sxs-lookup"><span data-stu-id="b55e3-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="b55e3-106">Controles de edição avançados sem janela recebem essa funcionalidade por meio de um par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="b55e3-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b55e3-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="b55e3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b55e3-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="b55e3-108">Technologies</span></span>

-   [<span data-ttu-id="b55e3-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="b55e3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b55e3-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b55e3-110">Prerequisites</span></span>

-   <span data-ttu-id="b55e3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b55e3-111">C/C++</span></span>
-   <span data-ttu-id="b55e3-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="b55e3-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b55e3-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="b55e3-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="b55e3-114">Estabelecer a funcionalidade da janela</span><span class="sxs-lookup"><span data-stu-id="b55e3-114">Establish the Window Functionality</span></span>

<span data-ttu-id="b55e3-115">O código de exemplo a seguir demonstra como criar o host de texto e os serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="b55e3-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="b55e3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b55e3-116">Remarks</span></span>

<span data-ttu-id="b55e3-117">O parâmetro *hmodRichEdit* no exemplo de código é um identificador para o módulo Msftedit.dll, e supõe-se que esse identificador já tenha sido recuperado por uma chamada para a função **GetModuleHandle** .</span><span class="sxs-lookup"><span data-stu-id="b55e3-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="b55e3-118">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="b55e3-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="b55e3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b55e3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b55e3-120">Usando controles de edição avançados sem janela</span><span class="sxs-lookup"><span data-stu-id="b55e3-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="b55e3-121">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="b55e3-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="b55e3-122">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="b55e3-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




