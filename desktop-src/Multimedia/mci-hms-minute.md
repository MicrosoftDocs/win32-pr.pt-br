---
title: Macro MCI_HMS_MINUTE (Mciapi. h)
description: A \_ macro HMS \_ minute do MCI recupera o componente de minutos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- Multimídia MCI_HMS_MINUTE macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086399"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="cbcaf-104">\_Macro de \_ minuto HMS MCI</span><span class="sxs-lookup"><span data-stu-id="cbcaf-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="cbcaf-105">A **macro \_ HMS \_ minute do MCI** recupera o componente de minutos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.</span><span class="sxs-lookup"><span data-stu-id="cbcaf-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcaf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbcaf-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="cbcaf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbcaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcaf-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="cbcaf-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="cbcaf-109">Hora no formato HMS.</span><span class="sxs-lookup"><span data-stu-id="cbcaf-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcaf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbcaf-110">Return value</span></span>

<span data-ttu-id="cbcaf-111">Retorna o componente de minutos das informações de HMS especificadas.</span><span class="sxs-lookup"><span data-stu-id="cbcaf-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcaf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbcaf-112">Remarks</span></span>

<span data-ttu-id="cbcaf-113">O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos.</span><span class="sxs-lookup"><span data-stu-id="cbcaf-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="cbcaf-114">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="cbcaf-114">The most significant byte is unused.</span></span>

<span data-ttu-id="cbcaf-115">A macro **MCI \_ HMS \_ minute** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cbcaf-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="cbcaf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbcaf-116">Requirements</span></span>



| <span data-ttu-id="cbcaf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbcaf-117">Requirement</span></span> | <span data-ttu-id="cbcaf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cbcaf-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcaf-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbcaf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cbcaf-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cbcaf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cbcaf-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbcaf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cbcaf-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cbcaf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cbcaf-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cbcaf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbcaf-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbcaf-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbcaf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbcaf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcaf-126">MCI</span><span class="sxs-lookup"><span data-stu-id="cbcaf-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cbcaf-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="cbcaf-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





