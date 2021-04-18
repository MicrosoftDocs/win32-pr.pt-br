---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: O MCI \_ Make \_ TMSF macro cria um valor de tempo no formato de faixas/minutos/segundos/quadros (TMSF) fornecidos a partir de determinados valores de faixas, minutos, segundos e quadros.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- Multimídia MCI_MAKE_TMSF macro do Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770161"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="14b26-104">\_Macro Make \_ TMSF do MCI</span><span class="sxs-lookup"><span data-stu-id="14b26-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="14b26-105">O **MCI \_ Make \_ TMSF** macro cria um valor de tempo no formato de faixas/minutos/segundos/quadros (TMSF) fornecidos a partir de determinados valores de faixas, minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="14b26-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b26-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14b26-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="14b26-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14b26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b26-108">*faixas*</span><span class="sxs-lookup"><span data-stu-id="14b26-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="14b26-109">Número de faixas.</span><span class="sxs-lookup"><span data-stu-id="14b26-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="14b26-110">*alguns*</span><span class="sxs-lookup"><span data-stu-id="14b26-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="14b26-111">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="14b26-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="14b26-112">*segundos*</span><span class="sxs-lookup"><span data-stu-id="14b26-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="14b26-113">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="14b26-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="14b26-114">*molduras*</span><span class="sxs-lookup"><span data-stu-id="14b26-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="14b26-115">Número de quadros.</span><span class="sxs-lookup"><span data-stu-id="14b26-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b26-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14b26-116">Return value</span></span>

<span data-ttu-id="14b26-117">Retorna o tempo no formato TMSF empacotado.</span><span class="sxs-lookup"><span data-stu-id="14b26-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b26-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="14b26-118">Remarks</span></span>

<span data-ttu-id="14b26-119">O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.</span><span class="sxs-lookup"><span data-stu-id="14b26-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="14b26-120">A **macro \_ Make \_ TMSF do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="14b26-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="14b26-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14b26-121">Requirements</span></span>



| <span data-ttu-id="14b26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b26-122">Requirement</span></span> | <span data-ttu-id="14b26-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14b26-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14b26-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14b26-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14b26-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14b26-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="14b26-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14b26-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14b26-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14b26-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14b26-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="14b26-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b26-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="14b26-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b26-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="14b26-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b26-131">MCI</span><span class="sxs-lookup"><span data-stu-id="14b26-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="14b26-132">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="14b26-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





