---
description: Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.
title: Função de retorno de chamada FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842237"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="af9e4-103">Função de retorno de chamada FMExtensionProc</span><span class="sxs-lookup"><span data-stu-id="af9e4-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="af9e4-104">Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af9e4-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af9e4-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="af9e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af9e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9e4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="af9e4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="af9e4-108">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="af9e4-108">Type: **HWND**</span></span>

<span data-ttu-id="af9e4-109">Um identificador de janela para o Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af9e4-109">A window handle to File Manager.</span></span> <span data-ttu-id="af9e4-110">Uma extensão usa esse identificador para especificar a janela pai de qualquer caixa de diálogo ou caixa de mensagem que deve ser exibida e para enviar mensagens de consulta ao Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af9e4-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="af9e4-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="af9e4-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="af9e4-112">Type: **WORD**</span></span>

<span data-ttu-id="af9e4-113">Uma das mensagens do Gerenciador de arquivos a seguir.</span><span class="sxs-lookup"><span data-stu-id="af9e4-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="af9e4-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 a 99**</span><span class="sxs-lookup"><span data-stu-id="af9e4-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-115">O usuário selecionou um item no menu fornecido pela extensão.</span><span class="sxs-lookup"><span data-stu-id="af9e4-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="af9e4-116">O valor é o identificador do item de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="af9e4-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="af9e4-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="af9e4-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-118">O usuário pressionou F1 ao selecionar um menu de extensão ou um item de comando de barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="af9e4-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="af9e4-119">Indica que a extensão deve chamar **WinHelp** adequadamente para o item de comando.</span><span class="sxs-lookup"><span data-stu-id="af9e4-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="af9e4-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HelpString**</span><span class="sxs-lookup"><span data-stu-id="af9e4-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-121">O usuário selecionou um menu de extensão ou um item de comando de barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="af9e4-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="af9e4-122">Indica que a extensão deve fornecer uma cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="af9e4-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="af9e4-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="af9e4-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-124">O usuário selecionou o menu da extensão.</span><span class="sxs-lookup"><span data-stu-id="af9e4-124">User selected the extension's menu.</span></span> <span data-ttu-id="af9e4-125">A extensão deve inicializar itens no menu.</span><span class="sxs-lookup"><span data-stu-id="af9e4-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="af9e4-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**</span><span class="sxs-lookup"><span data-stu-id="af9e4-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-127">O Gerenciador de Arquivos está carregando a DLL de extensão e solicita à DLL informações sobre o menu que a DLL fornece.</span><span class="sxs-lookup"><span data-stu-id="af9e4-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="af9e4-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="af9e4-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-129">A seleção na janela **de diretório do Gerenciador** de Arquivos ou na janela Resultados **da** Pesquisa foi alterada.</span><span class="sxs-lookup"><span data-stu-id="af9e4-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="af9e4-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**BARRA DE FERRAMENTAS \_ FMEVENTLOAD**</span><span class="sxs-lookup"><span data-stu-id="af9e4-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-131">O Gerenciador de Arquivos está criando a barra de ferramentas e solicita à DLL de extensão informações sobre os botões que a DLL adiciona à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="af9e4-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="af9e4-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**</span><span class="sxs-lookup"><span data-stu-id="af9e4-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-133">O Gerenciador de Arquivos está descarregando a DLL de extensão.</span><span class="sxs-lookup"><span data-stu-id="af9e4-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="af9e4-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ATUALIZAÇÃO DO USUÁRIO \_ \_ FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="af9e4-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="af9e4-135">O usuário **selecionou o** comando Atualizar no menu **Janela.**</span><span class="sxs-lookup"><span data-stu-id="af9e4-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="af9e4-136">A extensão deve atualizar itens no menu, se necessário.</span><span class="sxs-lookup"><span data-stu-id="af9e4-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="af9e4-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af9e4-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af9e4-138">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="af9e4-138">Type: **LONG**</span></span>

<span data-ttu-id="af9e4-139">Valor específico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="af9e4-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9e4-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af9e4-140">Return value</span></span>

<span data-ttu-id="af9e4-141">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="af9e4-141">Type: **LONG**</span></span>

<span data-ttu-id="af9e4-142">Retorna um valor dependente da mensagem *de parâmetro wMsg.*</span><span class="sxs-lookup"><span data-stu-id="af9e4-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9e4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af9e4-143">Requirements</span></span>



| <span data-ttu-id="af9e4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9e4-144">Requirement</span></span> | <span data-ttu-id="af9e4-145">Valor</span><span class="sxs-lookup"><span data-stu-id="af9e4-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af9e4-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af9e4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="af9e4-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="af9e4-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af9e4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="af9e4-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="af9e4-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af9e4-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9e4-151"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="af9e4-152">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="af9e4-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="af9e4-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="af9e4-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




