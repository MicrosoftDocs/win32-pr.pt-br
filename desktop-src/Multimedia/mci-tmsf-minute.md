---
title: Macro MCI_TMSF_MINUTE (Mciapi. h)
description: A \_ macro TMSF \_ minute do MCI recupera o componente de minutos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- Multimídia MCI_TMSF_MINUTE macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499387"
---
# <a name="mci_tmsf_minute-macro"></a><span data-ttu-id="951ca-104">\_Macro de \_ minuto TMSF MCI</span><span class="sxs-lookup"><span data-stu-id="951ca-104">MCI\_TMSF\_MINUTE macro</span></span>

<span data-ttu-id="951ca-105">A **macro \_ TMSF \_ minute do MCI** recupera o componente de minutos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.</span><span class="sxs-lookup"><span data-stu-id="951ca-105">The **MCI\_TMSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="951ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="951ca-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_MINUTE(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="951ca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="951ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="951ca-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="951ca-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="951ca-109">Hora no formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="951ca-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="951ca-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="951ca-110">Return value</span></span>

<span data-ttu-id="951ca-111">Retorna o componente de minutos das informações de TMSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="951ca-111">Returns the minutes component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="951ca-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="951ca-112">Remarks</span></span>

<span data-ttu-id="951ca-113">O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.</span><span class="sxs-lookup"><span data-stu-id="951ca-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="951ca-114">A macro **MCI \_ TMSF \_ minute** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="951ca-114">The **MCI\_TMSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="951ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="951ca-115">Requirements</span></span>



| <span data-ttu-id="951ca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="951ca-116">Requirement</span></span> | <span data-ttu-id="951ca-117">Valor</span><span class="sxs-lookup"><span data-stu-id="951ca-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="951ca-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="951ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="951ca-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="951ca-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="951ca-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="951ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="951ca-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="951ca-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="951ca-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="951ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="951ca-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="951ca-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951ca-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="951ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951ca-125">MCI</span><span class="sxs-lookup"><span data-stu-id="951ca-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="951ca-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="951ca-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





