---
description: Inicia o monitoramento de inatividade.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Função BeginIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756514"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="c3186-103">Função BeginIdleDetection</span><span class="sxs-lookup"><span data-stu-id="c3186-103">BeginIdleDetection function</span></span>

<span data-ttu-id="c3186-104">\[Essa função não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="c3186-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c3186-105">Em vez disso, use a função **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="c3186-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="c3186-106">Inicia o monitoramento de inatividade.</span><span class="sxs-lookup"><span data-stu-id="c3186-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3186-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3186-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="c3186-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3186-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3186-109">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="c3186-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="c3186-110">A função que é chamada quando o estado ocioso é alterado.</span><span class="sxs-lookup"><span data-stu-id="c3186-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="c3186-111">Esse retorno de chamada é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3186-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="c3186-112">*dwIdleMin*</span><span class="sxs-lookup"><span data-stu-id="c3186-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="c3186-113">O número de minutos de inatividade antes que a chamada seja feita para a função de chamada de retorno.</span><span class="sxs-lookup"><span data-stu-id="c3186-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c3186-114">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="c3186-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="c3186-115">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="c3186-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3186-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3186-116">Return value</span></span>

<span data-ttu-id="c3186-117">Retornará 0 se a função tiver sucesso; caso contrário, ele retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c3186-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="c3186-118">Por exemplo, se *dwReserved* for algo diferente de 0, **\_ \_ dados inválidos de erro** serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c3186-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3186-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3186-119">Remarks</span></span>

<span data-ttu-id="c3186-120">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c3186-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="c3186-121">Esta função não é exportada pelo nome; Especifique o ordinal 3 ao chamar **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="c3186-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3186-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3186-122">Requirements</span></span>



| <span data-ttu-id="c3186-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3186-123">Requirement</span></span> | <span data-ttu-id="c3186-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c3186-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3186-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c3186-125">DLL</span></span><br/> | <dl> <span data-ttu-id="c3186-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3186-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3186-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3186-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3186-128">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="c3186-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
