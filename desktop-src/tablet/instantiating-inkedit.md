---
description: Este tópico descreve as várias maneiras pelas quais você pode criar uma instância de um controle InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Instanciando InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461178"
---
# <a name="instantiating-inkedit"></a>Instanciando InkEdit

Este tópico descreve as várias maneiras pelas quais você pode criar uma instância de um controle [InkEdit](inkedit-control.md) .

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET e C\#

Se você estiver trabalhando com o Microsoft Visual Basic .NET ou C \# , arraste o controle [InkEdit](./inkedit-control.md) da caixa de ferramentas no Visual Studio para o formulário ou página onde você deseja que o controle apareça.

## <a name="win32c"></a>Win32/C++

O controle [InkEdit](inkedit-control-reference.md) é uma superclasse do controle de inserção de OLE do Win32 4,5 de edição avançada.

Os aplicativos Win32 instanciam o controle [InkEdit](inkedit-control-reference.md) chamando [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) e passando InkEdit como a classe Window. INKEDIT é definido em InkEd. h. Depois que o controle é criado, você pode "falar" com o controle com as mensagens. As mensagens de edição ricas (em \_ \* ) são passadas de InkEdit para edição rica inalterada; toda a funcionalidade de edição avançada existente está disponível.

Para criar um controle [InkEdit](inkedit-control-reference.md) , chame a função [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , especificando a classe de janela InkEdit. Use [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para registrar InkEd.dll. Especifique a \_ constante definida da classe INKEDIT para o parâmetro de classe de janela e use os estilos de janela, conforme especificado nos exemplos a seguir.

### <a name="instantiating-a-multiline-inkedit-control"></a>Criando uma instância de um controle InkEdit de várias linhas


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a>Instanciando um controle Single-Line InkEdit


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> Ao contrário de RichEdit, você deve ter certeza de chamar [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de criar o controle [InkEdit](inkedit-control-reference.md) . Chame [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) quando o aplicativo for desligado. Depois de chamar CoUninitialize (), você deve chamar [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para diminuir a contagem de referência no arquivo de InkEdit.dll.

 

Se você usar o estilo de janela [es \_ NOIME](../controls/rich-edit-control-styles.md) , o suporte interno à correção não estará disponível. Se você não especificar uma janela pai, o controle será criado como uma janela de nível superior e o \_ estilo WS SYSMENU será adicionado; isso também desabilita o suporte interno à correção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando controles de tinta a um projeto](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
