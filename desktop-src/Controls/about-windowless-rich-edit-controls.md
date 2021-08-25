---
title: Sobre controles de edição avançados sem janela
description: Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um controle de edição rico sem fornecer a janela.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b68a2bc0317a884f0516b73b3674d104c4fa6c12f16bdc24960d7ea0ef8bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922176"
---
# <a name="about-windowless-rich-edit-controls"></a>Sobre controles de edição avançados sem janela

Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um [controle de edição rico](rich-edit-controls.md) sem fornecer a janela. Para fornecer a funcionalidade de uma janela, como a capacidade de receber mensagens e um contexto de dispositivo no qual ele pode desenhar, os controles de edição avançados sem janela usam um par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Para criar um controle de edição rico sem janela, chame a função [**Createtextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) com um ponteiro para a implementação da interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) . **Createtextservices** retorna um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que você pode consultar para recuperar um ponteiro para a implementação [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) do controle sem janela.

Msftedit.dll exporta um IID (identificador de interface) chamado **IID \_ ITextServices** , que pode ser usado para consultar o ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) da interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . O exemplo a seguir mostra como recuperar **o \_ ITextServices de IID** e usá-lo para obter a interface **ITextServices** .


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



Msftedit.dll também exporta um IID (identificador de interface) chamado **IID \_ ITextHost** , que pode ser usado de maneira semelhante para consultar a interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .

A interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) tem métodos que o controle sem janela chama para recuperar informações sobre a janela. Por exemplo, o objeto de serviços de texto chama o método [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) para recuperar um contexto de dispositivo no qual ele pode desenhar. O controle sem janela chama o método [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) para enviar notificações, como as mensagens de notificação de edição rica, para o host de texto. O objeto de serviços de texto chama outros métodos **ITextHost** para solicitar que o host de texto execute outros serviços relacionados à janela. Por exemplo, o método [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) solicita que o host de texto adicione um retângulo à região de atualização da janela.

Um controle de edição avançada padrão tem um procedimento de janela que processa mensagens do sistema e mensagens do seu aplicativo. Você pode usar o identificador de janela do controle para enviar mensagens para executar a edição de texto e outras operações. Mas um controle de edição rico sem janela não tem nenhum procedimento de janela para receber e processar mensagens. Em vez disso, ele fornece uma interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Para enviar mensagens para um controle de edição rico sem janela, chame o método [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) . Você pode usar esse método para enviar qualquer uma das mensagens de edição avançadas ou para passar outras mensagens que afetam o controle, como mensagens do sistema para entrada de mouse ou de teclado.

Você também pode criar o objeto de serviços de texto como parte de um [objeto agregado com](/windows/desktop/com/aggregation). Isso facilita a agregação do objeto de serviços de texto com um objeto COM (Component Object Model sem janela).

 

 