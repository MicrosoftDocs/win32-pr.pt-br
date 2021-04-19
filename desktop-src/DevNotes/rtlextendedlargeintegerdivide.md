---
description: Divide inteiros estendidos.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: Função RtlExtendedLargeIntegerDivide
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756509"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="d5465-103">Função RtlExtendedLargeIntegerDivide</span><span class="sxs-lookup"><span data-stu-id="d5465-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="d5465-104">\[A função **RtlExtendedLargeIntegerDivide** é exportada para dar suporte a binários de driver existentes e é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d5465-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="d5465-105">Para obter um melhor desempenho, use o suporte do compilador para operações de inteiro de 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="d5465-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="d5465-106">Divide inteiros estendidos.</span><span class="sxs-lookup"><span data-stu-id="d5465-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5465-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5465-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="d5465-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5465-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5465-109">*Dividendo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5465-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5465-110">Cheque.</span><span class="sxs-lookup"><span data-stu-id="d5465-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="d5465-111">*Divisor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5465-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5465-112">Divisor.</span><span class="sxs-lookup"><span data-stu-id="d5465-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="d5465-113">*Restante* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d5465-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5465-114">Ponteiro para a divisão restante.</span><span class="sxs-lookup"><span data-stu-id="d5465-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5465-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5465-115">Return value</span></span>

<span data-ttu-id="d5465-116">Retorna o resultado da operação de divisão.</span><span class="sxs-lookup"><span data-stu-id="d5465-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5465-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5465-117">Remarks</span></span>

<span data-ttu-id="d5465-118">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d5465-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5465-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5465-119">Requirements</span></span>



| <span data-ttu-id="d5465-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5465-120">Requirement</span></span> | <span data-ttu-id="d5465-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d5465-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5465-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d5465-122">DLL</span></span><br/> | <dl> <span data-ttu-id="d5465-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5465-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
