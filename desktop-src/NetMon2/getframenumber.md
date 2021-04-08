---
description: A função GetFrameNumber retorna o número de um quadro.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Função GetFrameNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920697"
---
# <a name="getframenumber-function"></a><span data-ttu-id="44862-103">Função GetFrameNumber</span><span class="sxs-lookup"><span data-stu-id="44862-103">GetFrameNumber function</span></span>

<span data-ttu-id="44862-104">A função **GetFrameNumber** retorna o número de um quadro.</span><span class="sxs-lookup"><span data-stu-id="44862-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="44862-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44862-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="44862-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44862-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44862-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="44862-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44862-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="44862-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44862-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44862-109">Return value</span></span>

<span data-ttu-id="44862-110">Se a função for bem-sucedida, o valor de retorno será um número de quadro baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="44862-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="44862-111">Se a função não for bem-sucedida, o valor de retorno será menos um (-1).</span><span class="sxs-lookup"><span data-stu-id="44862-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="44862-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="44862-112">Remarks</span></span>

<span data-ttu-id="44862-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameNumber** .</span><span class="sxs-lookup"><span data-stu-id="44862-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="44862-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44862-114">Requirements</span></span>



| <span data-ttu-id="44862-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="44862-115">Requirement</span></span> | <span data-ttu-id="44862-116">Valor</span><span class="sxs-lookup"><span data-stu-id="44862-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44862-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44862-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44862-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44862-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44862-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44862-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44862-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44862-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44862-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44862-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44862-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44862-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="44862-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44862-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="44862-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44862-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="44862-125">DLL</span><span class="sxs-lookup"><span data-stu-id="44862-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44862-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44862-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




