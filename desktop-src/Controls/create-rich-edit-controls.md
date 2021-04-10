---
title: Como criar controles de edição avançados
description: Para criar um controle de edição rico, chame a função CreateWindowEx, especificando a classe da janela de edição rica.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008416"
---
# <a name="how-to-create-rich-edit-controls"></a>Como criar controles de edição avançados

Para criar um controle de edição rico, chame a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela de edição rica. Para o Microsoft rich edit 4,1 (Msftedit.dll), especifique \_ a classe MSFTEDIT como a classe de janela. Para todas as versões anteriores, especifique a \_ classe RichEdit. Para obter mais informações, consulte [versões do rich edit](about-rich-edit-controls.md).

Os controles de edição avançados dão suporte à maioria dos estilos de janela usados com controles de edição, bem como estilos adicionais. Você deve especificar o estilo de janela [**\_ multilinha es**](edit-control-styles.md) se desejar permitir mais de uma linha de texto no controle. Para obter mais informações, consulte [Rich Edit Control Styles](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="create-a-rich-edit-control"></a>Criar um controle de edição rico

A função de exemplo a seguir cria um controle de edição rico e o inicializa com algum texto.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



No Microsoft Visual Studio 2005 e posterior, é possível adicionar um controle de edição rico em um modelo de caixa de diálogo arrastando o controle da caixa de ferramentas. No entanto, fazer isso no editor de caixa de diálogo não garante que a biblioteca necessária será carregada antes de o controle ser criado. É necessário chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Riched32.dll, Riched20.dll ou Msftedit.dll antes de a caixa de diálogo ser criada.

## <a name="remarks"></a>Comentários

Para usar estilos visuais com esses controles, um aplicativo deve incluir um manifesto e deve chamar a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) no início do programa. Para obter informações sobre estilos visuais, consulte [estilos visuais](themes-overview.md). Para obter informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 