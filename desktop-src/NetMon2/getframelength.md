---
description: A função GetFrameLength retorna o comprimento do quadro.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Função GetFrameLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766847"
---
# <a name="getframelength-function"></a><span data-ttu-id="bd0d1-103">Função GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="bd0d1-103">GetFrameLength function</span></span>

<span data-ttu-id="bd0d1-104">A função **GetFrameLength** retorna o comprimento do quadro.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd0d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd0d1-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="bd0d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd0d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd0d1-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd0d1-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd0d1-108">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd0d1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd0d1-109">Return value</span></span>

<span data-ttu-id="bd0d1-110">Se a função for bem-sucedida, o valor de retorno será o comprimento do quadro em bytes.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="bd0d1-111">Se a função não for bem-sucedida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0d1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd0d1-112">Remarks</span></span>

<span data-ttu-id="bd0d1-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameLength** .</span><span class="sxs-lookup"><span data-stu-id="bd0d1-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0d1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd0d1-114">Requirements</span></span>



| <span data-ttu-id="bd0d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd0d1-115">Requirement</span></span> | <span data-ttu-id="bd0d1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bd0d1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0d1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0d1-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd0d1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bd0d1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0d1-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd0d1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bd0d1-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd0d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd0d1-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd0d1-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bd0d1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd0d1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd0d1-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd0d1-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd0d1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bd0d1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd0d1-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd0d1-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




