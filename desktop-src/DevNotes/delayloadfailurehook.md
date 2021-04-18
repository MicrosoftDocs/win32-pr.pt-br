---
description: Retorna o endereço de uma função de retorno de chamada de falha de carregamento de atraso para a DLL e o processo especificados.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Função DelayLoadFailureHook
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756218"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="613dc-103">Função DelayLoadFailureHook</span><span class="sxs-lookup"><span data-stu-id="613dc-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="613dc-104">Retorna o endereço de uma função de retorno de chamada de falha de carregamento de atraso para a DLL e o processo especificados.</span><span class="sxs-lookup"><span data-stu-id="613dc-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="613dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="613dc-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="613dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="613dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613dc-107">*pszDllName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="613dc-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613dc-108">O nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="613dc-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="613dc-109">*pszProcName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="613dc-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613dc-110">O nome do processo.</span><span class="sxs-lookup"><span data-stu-id="613dc-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613dc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="613dc-111">Return value</span></span>

<span data-ttu-id="613dc-112">O endereço da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="613dc-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="613dc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613dc-113">Requirements</span></span>



| <span data-ttu-id="613dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="613dc-114">Requirement</span></span> | <span data-ttu-id="613dc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="613dc-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="613dc-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="613dc-116">Library</span></span><br/> | <dl> <span data-ttu-id="613dc-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="613dc-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="613dc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="613dc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="613dc-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613dc-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613dc-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="613dc-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="613dc-121">[Ganchos de falha](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="613dc-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




