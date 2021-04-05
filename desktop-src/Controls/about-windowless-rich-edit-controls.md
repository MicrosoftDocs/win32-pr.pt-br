---
title: Sobre controles de edição avançados sem janela
description: Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um controle de edição rico sem fornecer a janela.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917698"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="cebd3-103">Sobre controles de edição avançados sem janela</span><span class="sxs-lookup"><span data-stu-id="cebd3-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="cebd3-104">Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um [controle de edição rico](rich-edit-controls.md) sem fornecer a janela.</span><span class="sxs-lookup"><span data-stu-id="cebd3-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="cebd3-105">Para fornecer a funcionalidade de uma janela, como a capacidade de receber mensagens e um contexto de dispositivo no qual ele pode desenhar, os controles de edição avançados sem janela usam um par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="cebd3-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="cebd3-106">Para criar um controle de edição rico sem janela, chame a função [**Createtextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) com um ponteiro para a implementação da interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="cebd3-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="cebd3-107">**Createtextservices** retorna um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que você pode consultar para recuperar um ponteiro para a implementação [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) do controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="cebd3-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="cebd3-108">Msftedit.dll exporta um IID (identificador de interface) chamado **IID \_ ITextServices** , que pode ser usado para consultar o ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) da interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="cebd3-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="cebd3-109">O exemplo a seguir mostra como recuperar **o \_ ITextServices de IID** e usá-lo para obter a interface **ITextServices** .</span><span class="sxs-lookup"><span data-stu-id="cebd3-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



<span data-ttu-id="cebd3-110">Msftedit.dll também exporta um IID (identificador de interface) chamado **IID \_ ITextHost** , que pode ser usado de maneira semelhante para consultar a interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="cebd3-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="cebd3-111">A interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) tem métodos que o controle sem janela chama para recuperar informações sobre a janela.</span><span class="sxs-lookup"><span data-stu-id="cebd3-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="cebd3-112">Por exemplo, o objeto de serviços de texto chama o método [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) para recuperar um contexto de dispositivo no qual ele pode desenhar.</span><span class="sxs-lookup"><span data-stu-id="cebd3-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="cebd3-113">O controle sem janela chama o método [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) para enviar notificações, como as mensagens de notificação de edição rica, para o host de texto.</span><span class="sxs-lookup"><span data-stu-id="cebd3-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="cebd3-114">O objeto de serviços de texto chama outros métodos **ITextHost** para solicitar que o host de texto execute outros serviços relacionados à janela.</span><span class="sxs-lookup"><span data-stu-id="cebd3-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="cebd3-115">Por exemplo, o método [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) solicita que o host de texto adicione um retângulo à região de atualização da janela.</span><span class="sxs-lookup"><span data-stu-id="cebd3-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="cebd3-116">Um controle de edição avançada padrão tem um procedimento de janela que processa mensagens do sistema e mensagens do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cebd3-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="cebd3-117">Você pode usar o identificador de janela do controle para enviar mensagens para executar a edição de texto e outras operações.</span><span class="sxs-lookup"><span data-stu-id="cebd3-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="cebd3-118">Mas um controle de edição rico sem janela não tem nenhum procedimento de janela para receber e processar mensagens.</span><span class="sxs-lookup"><span data-stu-id="cebd3-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="cebd3-119">Em vez disso, ele fornece uma interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="cebd3-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="cebd3-120">Para enviar mensagens para um controle de edição rico sem janela, chame o método [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) .</span><span class="sxs-lookup"><span data-stu-id="cebd3-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="cebd3-121">Você pode usar esse método para enviar qualquer uma das mensagens de edição avançadas ou para passar outras mensagens que afetam o controle, como mensagens do sistema para entrada de mouse ou de teclado.</span><span class="sxs-lookup"><span data-stu-id="cebd3-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="cebd3-122">Você também pode criar o objeto de serviços de texto como parte de um [objeto agregado com](/windows/desktop/com/aggregation).</span><span class="sxs-lookup"><span data-stu-id="cebd3-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="cebd3-123">Isso facilita a agregação do objeto de serviços de texto com um objeto COM (Component Object Model sem janela).</span><span class="sxs-lookup"><span data-stu-id="cebd3-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 