---
description: A função GetFrameStoredLength retorna o comprimento do quadro.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Função GetFrameStoredLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754318"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="31311-103">Função GetFrameStoredLength</span><span class="sxs-lookup"><span data-stu-id="31311-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="31311-104">A função **GetFrameStoredLength** retorna o comprimento do quadro.</span><span class="sxs-lookup"><span data-stu-id="31311-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="31311-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31311-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="31311-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31311-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31311-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31311-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31311-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="31311-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31311-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31311-109">Return value</span></span>

<span data-ttu-id="31311-110">Se a função for bem-sucedida, o valor de retorno será o comprimento do quadro como armazenado.</span><span class="sxs-lookup"><span data-stu-id="31311-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="31311-111">Se a função não for bem-sucedida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="31311-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="31311-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="31311-112">Remarks</span></span>

<span data-ttu-id="31311-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameStoredLength** .</span><span class="sxs-lookup"><span data-stu-id="31311-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="31311-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31311-114">Requirements</span></span>



| <span data-ttu-id="31311-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="31311-115">Requirement</span></span> | <span data-ttu-id="31311-116">Valor</span><span class="sxs-lookup"><span data-stu-id="31311-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31311-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31311-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31311-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31311-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="31311-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31311-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31311-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31311-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31311-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31311-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31311-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="31311-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="31311-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31311-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="31311-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31311-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="31311-125">DLL</span><span class="sxs-lookup"><span data-stu-id="31311-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31311-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31311-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31311-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="31311-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31311-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="31311-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




