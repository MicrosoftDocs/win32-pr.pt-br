---
title: Função GetProcessHandleFromHwnd
description: Recupera um identificador de processo de um identificador de janela.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Acessibilidade do Windows da função GetProcessHandleFromHwnd
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085602"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="7c75d-104">Função GetProcessHandleFromHwnd</span><span class="sxs-lookup"><span data-stu-id="7c75d-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="7c75d-105">Recupera um identificador de processo de um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="7c75d-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c75d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c75d-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="7c75d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c75d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c75d-108">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c75d-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c75d-109">Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c75d-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7c75d-110">O identificador da janela.</span><span class="sxs-lookup"><span data-stu-id="7c75d-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c75d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c75d-111">Return value</span></span>

<span data-ttu-id="7c75d-112">Tipo: **[ **identificador**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c75d-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7c75d-113">Se for bem-sucedido, retorna o identificador do processo que possui a janela.</span><span class="sxs-lookup"><span data-stu-id="7c75d-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="7c75d-114">Se não for bem-sucedido, retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7c75d-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c75d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c75d-115">Remarks</span></span>

<span data-ttu-id="7c75d-116">Em versões anteriores do sistema operacional, um processo poderia abrir outro processo (para acessar sua memória, por exemplo) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span><span class="sxs-lookup"><span data-stu-id="7c75d-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="7c75d-117">Essa função terá sucesso se o chamador tiver os privilégios apropriados; Normalmente, o chamador e o processo de destino devem ser o mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="7c75d-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="7c75d-118">No Windows Vista, no entanto, o [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) falha no cenário em que o chamador tem o UIAccess e o processo de destino é elevado.</span><span class="sxs-lookup"><span data-stu-id="7c75d-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="7c75d-119">Nesse caso, o proprietário do processo de destino está no grupo Administradores, mas o processo de chamada está sendo executado com o token restrito, portanto, não tem associação nesse grupo e tem acesso negado ao processo elevado.</span><span class="sxs-lookup"><span data-stu-id="7c75d-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="7c75d-120">No entanto, se o chamador tiver o UIAccess, ele poderá usar um gancho do Windows para injetar código no processo de destino e, no processo de destino, enviar um identificador de volta para o chamador.</span><span class="sxs-lookup"><span data-stu-id="7c75d-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="7c75d-121">**GetProcessHandleFromHwnd** é uma função de conveniência que usa essa técnica para obter o identificador do processo que possui o HWND especificado.</span><span class="sxs-lookup"><span data-stu-id="7c75d-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="7c75d-122">Observe que ele só é bem sucedido nos casos em que o chamador e o processo de destino estão sendo executados como o mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="7c75d-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="7c75d-123">O identificador retornado tem os seguintes privilégios: processo de identificador de DUP processo operação de VM processar processo de leitura da VM \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ gravação \| sincronizar.</span><span class="sxs-lookup"><span data-stu-id="7c75d-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="7c75d-124">Se outros privilégios forem necessários, talvez seja necessário implementar explicitamente a técnica de conexão em vez de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="7c75d-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c75d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c75d-125">Requirements</span></span>



| <span data-ttu-id="7c75d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c75d-126">Requirement</span></span> | <span data-ttu-id="7c75d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7c75d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c75d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c75d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c75d-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7c75d-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c75d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c75d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c75d-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c75d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c75d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7c75d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c75d-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c75d-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

