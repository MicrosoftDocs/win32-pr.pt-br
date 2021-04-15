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
# <a name="instantiating-inkedit"></a><span data-ttu-id="48ec5-103">Instanciando InkEdit</span><span class="sxs-lookup"><span data-stu-id="48ec5-103">Instantiating InkEdit</span></span>

<span data-ttu-id="48ec5-104">Este tópico descreve as várias maneiras pelas quais você pode criar uma instância de um controle [InkEdit](inkedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="48ec5-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="48ec5-105">Visual Basic .NET e C\#</span><span class="sxs-lookup"><span data-stu-id="48ec5-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="48ec5-106">Se você estiver trabalhando com o Microsoft Visual Basic .NET ou C \# , arraste o controle [InkEdit](./inkedit-control.md) da caixa de ferramentas no Visual Studio para o formulário ou página onde você deseja que o controle apareça.</span><span class="sxs-lookup"><span data-stu-id="48ec5-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="48ec5-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="48ec5-107">Win32/C++</span></span>

<span data-ttu-id="48ec5-108">O controle [InkEdit](inkedit-control-reference.md) é uma superclasse do controle de inserção de OLE do Win32 4,5 de edição avançada.</span><span class="sxs-lookup"><span data-stu-id="48ec5-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="48ec5-109">Os aplicativos Win32 instanciam o controle [InkEdit](inkedit-control-reference.md) chamando [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) e passando InkEdit como a classe Window.</span><span class="sxs-lookup"><span data-stu-id="48ec5-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="48ec5-110">INKEDIT é definido em InkEd. h.</span><span class="sxs-lookup"><span data-stu-id="48ec5-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="48ec5-111">Depois que o controle é criado, você pode "falar" com o controle com as mensagens.</span><span class="sxs-lookup"><span data-stu-id="48ec5-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="48ec5-112">As mensagens de edição ricas (em \_ \* ) são passadas de InkEdit para edição rica inalterada; toda a funcionalidade de edição avançada existente está disponível.</span><span class="sxs-lookup"><span data-stu-id="48ec5-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="48ec5-113">Para criar um controle [InkEdit](inkedit-control-reference.md) , chame a função [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , especificando a classe de janela InkEdit.</span><span class="sxs-lookup"><span data-stu-id="48ec5-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="48ec5-114">Use [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para registrar InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="48ec5-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="48ec5-115">Especifique a \_ constante definida da classe INKEDIT para o parâmetro de classe de janela e use os estilos de janela, conforme especificado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="48ec5-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="48ec5-116">Criando uma instância de um controle InkEdit de várias linhas</span><span class="sxs-lookup"><span data-stu-id="48ec5-116">Instantiating a Multiline InkEdit Control</span></span>


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



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="48ec5-117">Instanciando um controle Single-Line InkEdit</span><span class="sxs-lookup"><span data-stu-id="48ec5-117">Instantiating a Single-Line InkEdit Control</span></span>


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
> <span data-ttu-id="48ec5-118">Ao contrário de RichEdit, você deve ter certeza de chamar [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de criar o controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="48ec5-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="48ec5-119">Chame [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) quando o aplicativo for desligado.</span><span class="sxs-lookup"><span data-stu-id="48ec5-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="48ec5-120">Depois de chamar CoUninitialize (), você deve chamar [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para diminuir a contagem de referência no arquivo de InkEdit.dll.</span><span class="sxs-lookup"><span data-stu-id="48ec5-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="48ec5-121">Se você usar o estilo de janela [es \_ NOIME](../controls/rich-edit-control-styles.md) , o suporte interno à correção não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="48ec5-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="48ec5-122">Se você não especificar uma janela pai, o controle será criado como uma janela de nível superior e o \_ estilo WS SYSMENU será adicionado; isso também desabilita o suporte interno à correção.</span><span class="sxs-lookup"><span data-stu-id="48ec5-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48ec5-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48ec5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48ec5-124">Adicionando controles de tinta a um projeto</span><span class="sxs-lookup"><span data-stu-id="48ec5-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
