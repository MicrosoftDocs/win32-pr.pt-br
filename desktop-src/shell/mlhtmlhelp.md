---
description: Exibe uma janela de ajuda que corresponde à configuração de idioma da interface do usuário atual.
title: Função MLHtmlHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841207"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="3f073-103">Função MLHtmlHelp</span><span class="sxs-lookup"><span data-stu-id="3f073-103">MLHtmlHelp function</span></span>

<span data-ttu-id="3f073-104">\[Essa função está disponível por meio do Windows XP e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f073-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3f073-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f073-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3f073-106">Exibe uma janela de ajuda que corresponde à configuração de idioma da interface do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="3f073-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f073-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f073-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="3f073-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f073-109">*hwndCaller* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f073-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f073-110">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="3f073-110">Type: **HWND**</span></span>

<span data-ttu-id="3f073-111">Um identificador para a janela pai que chama essa função.</span><span class="sxs-lookup"><span data-stu-id="3f073-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="3f073-112">*pszFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f073-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f073-113">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="3f073-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="3f073-114">Um ponteiro para um buffer que contém o caminho totalmente qualificado de um arquivo de ajuda compilado (. chm) ou um arquivo de tópico dentro de um arquivo de ajuda especificado.</span><span class="sxs-lookup"><span data-stu-id="3f073-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="3f073-115">*uCommand* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f073-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f073-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f073-116">Type: **UINT**</span></span>

<span data-ttu-id="3f073-117">O comando a ser concluído.</span><span class="sxs-lookup"><span data-stu-id="3f073-117">The command to complete.</span></span> <span data-ttu-id="3f073-118">Essa função dá suporte diretamente somente ao [ \_ \_ tópico de exibição hh](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) e ao [ \_ \_ \_ pop-up exibir texto](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="3f073-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="3f073-119">No caso de qualquer outro comando, a chamada é encaminhada sem o valor de *dwCrossCodePage* para [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="3f073-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="3f073-120">*dwData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f073-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f073-121">Tipo: **DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="3f073-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="3f073-122">Todos os dados que podem ser necessários, com base no valor do parâmetro *uCommand* .</span><span class="sxs-lookup"><span data-stu-id="3f073-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3f073-123">*dwCrossCodePage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f073-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f073-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3f073-124">Type: **DWORD**</span></span>

<span data-ttu-id="3f073-125">O **valor DWORD** que indica a página de código da configuração de linguagem de interface do usuário atual, como CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="3f073-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f073-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f073-126">Return value</span></span>

<span data-ttu-id="3f073-127">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="3f073-127">Type: **HWND**</span></span>

<span data-ttu-id="3f073-128">Dependendo do *uCommand* especificado e do resultado, **MLHtmlHelp** retorna um ou ambos os seguintes:</span><span class="sxs-lookup"><span data-stu-id="3f073-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="3f073-129">O handle (hwnd) da janela de ajuda.</span><span class="sxs-lookup"><span data-stu-id="3f073-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="3f073-130">**NULL**.</span><span class="sxs-lookup"><span data-stu-id="3f073-130">**NULL**.</span></span> <span data-ttu-id="3f073-131">Em alguns casos, **NULL** indica falha; em outros casos, **NULL** indica que a janela de ajuda ainda não foi criada.</span><span class="sxs-lookup"><span data-stu-id="3f073-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f073-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f073-132">Remarks</span></span>

<span data-ttu-id="3f073-133">Se surgir um problema com o caminho do arquivo de ajuda para a linguagem atual, a chamada será encaminhada para [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para manipulação padrão.</span><span class="sxs-lookup"><span data-stu-id="3f073-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="3f073-134">Quando a janela de ajuda é fechada, o foco retorna para o proprietário, a menos que o proprietário seja a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3f073-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="3f073-135">Se *hwndCaller for* a área de trabalho, o sistema operacional determinará onde o foco será retornado.</span><span class="sxs-lookup"><span data-stu-id="3f073-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="3f073-136">Além disso, se **MLHtmlHelp** enviar qualquer mensagem de notificação da janela de ajuda, as [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) mensagens serão enviadas para *hwndCaller,* desde que você tenha habilitado o acompanhamento de mensagens de notificação na definição da janela de ajuda.</span><span class="sxs-lookup"><span data-stu-id="3f073-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="3f073-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f073-137">Examples</span></span>

<span data-ttu-id="3f073-138">O exemplo a seguir chama o comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir o arquivo de ajuda chamado Help.chm e exibir seu tópico padrão na janela de ajuda chamada `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="3f073-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="3f073-139">Em geral, a janela de ajuda especificada neste comando é um [Visualizador da Ajuda HTML padrão.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)</span><span class="sxs-lookup"><span data-stu-id="3f073-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="3f073-140">Ao usar essa função, de definido o tamanho da pilha do executável de hospedagem como pelo menos 100 mil.</span><span class="sxs-lookup"><span data-stu-id="3f073-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="3f073-141">Se o tamanho da pilha definido for muito pequeno, o thread criado para executar a Ajuda HTML também será criado com esse tamanho de pilha e a operação poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="3f073-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="3f073-142">Opcionalmente, você pode remover /STACK da linha de comando do link e também remover qualquer configuração stack no arquivo DEF do executável (nesse caso, o tamanho padrão da pilha é de 1 MB).</span><span class="sxs-lookup"><span data-stu-id="3f073-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="3f073-143">Você também pode definir o tamanho da pilha usando o comando do compilador /Fnumber (o compilador passará isso para o linker como /STACK).</span><span class="sxs-lookup"><span data-stu-id="3f073-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f073-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f073-144">Requirements</span></span>



| <span data-ttu-id="3f073-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f073-145">Requirement</span></span> | <span data-ttu-id="3f073-146">Valor</span><span class="sxs-lookup"><span data-stu-id="3f073-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f073-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f073-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3f073-148">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3f073-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f073-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f073-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3f073-150">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f073-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3f073-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f073-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f073-152"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="3f073-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="3f073-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3f073-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f073-154"><dt>Shlwapi.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3f073-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3f073-155">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3f073-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3f073-156">**MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3f073-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
