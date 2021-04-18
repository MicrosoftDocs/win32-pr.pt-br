---
description: Encaminha os eventos do objeto ShellFolderView especificado para o manipulador de eventos ShellFolderViewOC correspondente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Método ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968118"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="446b8-103">Método ShellFolderViewOC. SetFolderView</span><span class="sxs-lookup"><span data-stu-id="446b8-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="446b8-104">Encaminha os eventos do objeto [**ShellFolderView**](shellfolderview.md) especificado para o manipulador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="446b8-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="446b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="446b8-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="446b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="446b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="446b8-107">*oShellFolderView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="446b8-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="446b8-108">Tipo: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="446b8-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="446b8-109">Um objeto [_ *ShellFolderView* \*](shellfolderview.md) .</span><span class="sxs-lookup"><span data-stu-id="446b8-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="446b8-110">Seus eventos [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderview-selectionchanged.md) serão encaminhados para o manipulador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="446b8-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="446b8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="446b8-111">Requirements</span></span>



| <span data-ttu-id="446b8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="446b8-112">Requirement</span></span> | <span data-ttu-id="446b8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="446b8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="446b8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="446b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="446b8-115">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="446b8-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="446b8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="446b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="446b8-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="446b8-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="446b8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="446b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="446b8-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="446b8-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="446b8-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="446b8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="446b8-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="446b8-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="446b8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="446b8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="446b8-123"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="446b8-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
