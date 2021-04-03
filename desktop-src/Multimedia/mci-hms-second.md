---
title: Macro MCI_HMS_SECOND (Mciapi. h)
description: A \_ segunda macro do MCI HMS \_ recupera o componente de segundos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- Multimídia MCI_HMS_SECOND macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824787"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="1ebdf-104">\_Macro da \_ segunda HMS MCI</span><span class="sxs-lookup"><span data-stu-id="1ebdf-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="1ebdf-105">A **\_ \_ segunda macro do MCI HMS** recupera o componente de segundos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebdf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ebdf-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="1ebdf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ebdf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ebdf-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="1ebdf-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="1ebdf-109">Hora no formato HMS.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ebdf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ebdf-110">Return value</span></span>

<span data-ttu-id="1ebdf-111">Retorna o componente de segundos das informações de HMS especificadas.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ebdf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ebdf-112">Remarks</span></span>

<span data-ttu-id="1ebdf-113">O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="1ebdf-114">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-114">The most significant byte is unused.</span></span>

<span data-ttu-id="1ebdf-115">A **\_ \_ segunda macro HMS do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1ebdf-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="1ebdf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ebdf-116">Requirements</span></span>



| <span data-ttu-id="1ebdf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ebdf-117">Requirement</span></span> | <span data-ttu-id="1ebdf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebdf-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebdf-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ebdf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebdf-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ebdf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ebdf-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ebdf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebdf-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ebdf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ebdf-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ebdf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ebdf-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdf-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ebdf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ebdf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebdf-126">MCI</span><span class="sxs-lookup"><span data-stu-id="1ebdf-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1ebdf-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="1ebdf-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





