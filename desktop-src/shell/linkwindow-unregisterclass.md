---
description: Cancela o registro de uma classe de janela registrada pela LinkWindow \_ RegisterClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: Função LinkWindow_UnregisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968017"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="be31c-103">\_Função UnregisterClass de LinkWindow</span><span class="sxs-lookup"><span data-stu-id="be31c-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="be31c-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="be31c-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="be31c-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be31c-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="be31c-106">Cancela o registro de uma classe de janela registrada pela [**LinkWindow \_ registerClass**](linkwindow-registerclass.md).</span><span class="sxs-lookup"><span data-stu-id="be31c-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be31c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be31c-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="be31c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be31c-108">Parameters</span></span>

<span data-ttu-id="be31c-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="be31c-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be31c-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be31c-110">Return value</span></span>

<span data-ttu-id="be31c-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="be31c-111">Type: **BOOL**</span></span>

<span data-ttu-id="be31c-112">Retorna **true** se a operação foi bem-sucedida; Caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="be31c-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="be31c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be31c-113">Remarks</span></span>

<span data-ttu-id="be31c-114">Essa função não tem um cabeçalho ou arquivo de biblioteca associado, portanto, ele deve ser chamado pelo valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="be31c-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="be31c-115">Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da dll Shell32.dll para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="be31c-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="be31c-116">Em seguida, chame [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o número ordinal 259 para usar essa função.</span><span class="sxs-lookup"><span data-stu-id="be31c-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be31c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be31c-117">Requirements</span></span>



| <span data-ttu-id="be31c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be31c-118">Requirement</span></span> | <span data-ttu-id="be31c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="be31c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be31c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be31c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="be31c-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be31c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be31c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be31c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="be31c-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be31c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="be31c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="be31c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be31c-125"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="be31c-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be31c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="be31c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be31c-127">Visão geral dos controles SysLink</span><span class="sxs-lookup"><span data-stu-id="be31c-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
