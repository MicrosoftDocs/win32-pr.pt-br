---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: O MCI \_ criar \_ macro do MSF cria um valor de tempo no formato de minutos/segundos/quadros empacotado a partir dos minutos, segundos e valores de quadro determinados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- Multimídia MCI_MAKE_MSF macro do Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919142"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="8adf3-104">\_Macro do \_ MSF Make MCI</span><span class="sxs-lookup"><span data-stu-id="8adf3-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="8adf3-105">O **MCI \_ criar \_** macro do MSF cria um valor de tempo no formato de minutos/segundos/quadros empacotado a partir dos minutos, segundos e valores de quadro determinados.</span><span class="sxs-lookup"><span data-stu-id="8adf3-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adf3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8adf3-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="8adf3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8adf3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adf3-108">*alguns*</span><span class="sxs-lookup"><span data-stu-id="8adf3-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="8adf3-109">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="8adf3-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="8adf3-110">*segundos*</span><span class="sxs-lookup"><span data-stu-id="8adf3-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="8adf3-111">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="8adf3-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="8adf3-112">*molduras*</span><span class="sxs-lookup"><span data-stu-id="8adf3-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="8adf3-113">Número de quadros.</span><span class="sxs-lookup"><span data-stu-id="8adf3-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adf3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8adf3-114">Return value</span></span>

<span data-ttu-id="8adf3-115">Retorna o tempo no formato empacotado do MSF.</span><span class="sxs-lookup"><span data-stu-id="8adf3-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="8adf3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8adf3-116">Remarks</span></span>

<span data-ttu-id="8adf3-117">O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros.</span><span class="sxs-lookup"><span data-stu-id="8adf3-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="8adf3-118">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="8adf3-118">The most significant byte is unused.</span></span>

<span data-ttu-id="8adf3-119">O **MCI \_ criar \_** macro do MSF é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8adf3-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="8adf3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adf3-120">Requirements</span></span>



| <span data-ttu-id="8adf3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adf3-121">Requirement</span></span> | <span data-ttu-id="8adf3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8adf3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8adf3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adf3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8adf3-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8adf3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8adf3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adf3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8adf3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8adf3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8adf3-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8adf3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8adf3-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adf3-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8adf3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8adf3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adf3-130">MCI</span><span class="sxs-lookup"><span data-stu-id="8adf3-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8adf3-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="8adf3-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





