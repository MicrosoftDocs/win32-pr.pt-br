---
description: Multiplica os inteiros estendidos.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Função RtlExtendedIntegerMultiply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755511"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="92a9b-103">Função RtlExtendedIntegerMultiply</span><span class="sxs-lookup"><span data-stu-id="92a9b-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="92a9b-104">\[A função **RtlExtendedIntegerMultiply** é exportada para dar suporte a binários de driver existentes e é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="92a9b-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="92a9b-105">Para obter um melhor desempenho, use o suporte do compilador para operações de inteiro de 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="92a9b-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="92a9b-106">Multiplica os inteiros estendidos.</span><span class="sxs-lookup"><span data-stu-id="92a9b-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a9b-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="92a9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a9b-109">*Multiplicando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92a9b-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a9b-110">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="92a9b-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="92a9b-111">*Multiplicador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92a9b-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a9b-112">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="92a9b-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a9b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92a9b-113">Return value</span></span>

<span data-ttu-id="92a9b-114">Retorna o resultado da multiplicação.</span><span class="sxs-lookup"><span data-stu-id="92a9b-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a9b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a9b-115">Remarks</span></span>

<span data-ttu-id="92a9b-116">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="92a9b-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a9b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a9b-117">Requirements</span></span>



| <span data-ttu-id="92a9b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a9b-118">Requirement</span></span> | <span data-ttu-id="92a9b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="92a9b-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92a9b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="92a9b-120">DLL</span></span><br/> | <dl> <span data-ttu-id="92a9b-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a9b-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
