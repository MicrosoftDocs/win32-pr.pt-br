---
description: Registra uma classe de janela que permite que o controle comum SysLink seja usado em uma janela.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Função LinkWindow_RegisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968018"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="4aef1-103">\_Função registerClass LinkWindow</span><span class="sxs-lookup"><span data-stu-id="4aef1-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="4aef1-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4aef1-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="4aef1-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="4aef1-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="4aef1-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="4aef1-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="4aef1-107">Registra uma classe de janela que permite que o controle comum [Syslink](../controls/syslink-overview.md) seja usado em uma janela.</span><span class="sxs-lookup"><span data-stu-id="4aef1-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aef1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4aef1-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="4aef1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4aef1-109">Parameters</span></span>

<span data-ttu-id="4aef1-110">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4aef1-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aef1-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4aef1-111">Return value</span></span>

<span data-ttu-id="4aef1-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="4aef1-112">Type: **BOOL**</span></span>

<span data-ttu-id="4aef1-113">Retornará **true** se o registro tiver sido bem-sucedido; Caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="4aef1-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aef1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4aef1-114">Remarks</span></span>

<span data-ttu-id="4aef1-115">Essa função não tem um cabeçalho ou arquivo de biblioteca associado, portanto, ele deve ser chamado pelo valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="4aef1-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="4aef1-116">Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da dll Shell32.dll para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="4aef1-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="4aef1-117">Em seguida, chame [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o número ordinal 258 para usar essa função.</span><span class="sxs-lookup"><span data-stu-id="4aef1-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="4aef1-118">Use [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) para cancelar o registro da classe após o uso.</span><span class="sxs-lookup"><span data-stu-id="4aef1-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aef1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aef1-119">Requirements</span></span>



| <span data-ttu-id="4aef1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aef1-120">Requirement</span></span> | <span data-ttu-id="4aef1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4aef1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aef1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aef1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4aef1-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4aef1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4aef1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aef1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4aef1-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4aef1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4aef1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4aef1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aef1-127"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4aef1-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aef1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aef1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aef1-129">Visão geral dos controles SysLink</span><span class="sxs-lookup"><span data-stu-id="4aef1-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
