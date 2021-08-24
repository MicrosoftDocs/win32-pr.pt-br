---
title: Como fornecer controles de edição avançados sem janelas com a funcionalidade de janela
description: A funcionalidade de janela inclui a capacidade de receber mensagens e a propriedade de um contexto de dispositivo no qual desenhar. Controles de edição avançados sem janela recebem essa funcionalidade por meio de um par de interfaces ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698596"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Como fornecer controles de edição avançados sem janelas com a funcionalidade de janela

A funcionalidade de janela inclui a capacidade de receber mensagens e a propriedade de um contexto de dispositivo no qual desenhar. Controles de edição avançados sem janela recebem essa funcionalidade por meio de um par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="establish-the-window-functionality"></a>Estabelecer a funcionalidade da janela

O código de exemplo a seguir demonstra como criar o host de texto e os serviços de texto.


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



## <a name="remarks"></a>Comentários

O parâmetro *hmodRichEdit* no exemplo de código é um identificador para o módulo Msftedit.dll, e supõe-se que esse identificador já tenha sido recuperado por uma chamada para a função **GetModuleHandle** .

## <a name="complete-example"></a>Exemplo completo

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados sem janela](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




