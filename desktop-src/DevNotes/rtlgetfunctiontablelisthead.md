---
description: Permite que um depurador examine informações de tabela de funções dinâmicas.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Função RtlGetFunctionTableListHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771771"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="cae6e-103">Função RtlGetFunctionTableListHead</span><span class="sxs-lookup"><span data-stu-id="cae6e-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="cae6e-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="cae6e-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="cae6e-105">Permite que um depurador examine informações de tabela de funções dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="cae6e-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae6e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cae6e-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="cae6e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cae6e-107">Parameters</span></span>

<span data-ttu-id="cae6e-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cae6e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cae6e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cae6e-109">Return value</span></span>

<span data-ttu-id="cae6e-110">Retorna um ponteiro para o cabeçalho da lista de tabelas de funções.</span><span class="sxs-lookup"><span data-stu-id="cae6e-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae6e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae6e-111">Remarks</span></span>

<span data-ttu-id="cae6e-112">Observe que o arquivo de cabeçalho do WDK (Windows Driver Kit) Ntdef. h é necessário para algumas definições.</span><span class="sxs-lookup"><span data-stu-id="cae6e-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="cae6e-113">A biblioteca de importação associada, ntdll. lib, está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="cae6e-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="cae6e-114">Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="cae6e-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae6e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cae6e-115">Requirements</span></span>



| <span data-ttu-id="cae6e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae6e-116">Requirement</span></span> | <span data-ttu-id="cae6e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cae6e-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cae6e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cae6e-118">DLL</span></span><br/> | <dl> <span data-ttu-id="cae6e-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae6e-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
