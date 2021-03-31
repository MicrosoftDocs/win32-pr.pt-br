---
title: Macro MCI_MAKE_HMS (Mciapi. h)
description: O MCI \_ Make \_ HMS macro cria um valor de tempo no formato de horas/minutos/segundos (HMS) empacotado dos valores de horas, minutos e segundos fornecidos.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- Multimídia MCI_MAKE_HMS macro do Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645060"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="ebfb4-104">\_Macro Make \_ HMS do MCI</span><span class="sxs-lookup"><span data-stu-id="ebfb4-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="ebfb4-105">O **MCI \_ Make \_ HMS** macro cria um valor de tempo no formato de horas/minutos/segundos (HMS) empacotado dos valores de horas, minutos e segundos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfb4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebfb4-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="ebfb4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebfb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfb4-108">*duração*</span><span class="sxs-lookup"><span data-stu-id="ebfb4-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfb4-109">Número de horas.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="ebfb4-110">*alguns*</span><span class="sxs-lookup"><span data-stu-id="ebfb4-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfb4-111">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="ebfb4-112">*segundos*</span><span class="sxs-lookup"><span data-stu-id="ebfb4-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfb4-113">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfb4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebfb4-114">Return value</span></span>

<span data-ttu-id="ebfb4-115">Retorna o tempo no formato HMS empacotado.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebfb4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebfb4-116">Remarks</span></span>

<span data-ttu-id="ebfb4-117">O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="ebfb4-118">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-118">The most significant byte is unused.</span></span>

<span data-ttu-id="ebfb4-119">A **macro \_ Make \_ HMS do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ebfb4-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="ebfb4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebfb4-120">Requirements</span></span>



| <span data-ttu-id="ebfb4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebfb4-121">Requirement</span></span> | <span data-ttu-id="ebfb4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ebfb4-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfb4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebfb4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfb4-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebfb4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ebfb4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebfb4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfb4-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebfb4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ebfb4-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ebfb4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebfb4-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfb4-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebfb4-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ebfb4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfb4-130">MCI</span><span class="sxs-lookup"><span data-stu-id="ebfb4-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ebfb4-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="ebfb4-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





