---
title: Macro MCI_TMSF_FRAME (Mciapi. h)
description: A \_ macro do quadro MCI TMSF \_ recupera o componente de quadros de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- Multimídia MCI_TMSF_FRAME macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644338"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="94876-104">\_Macro do \_ quadro MCI TMSF</span><span class="sxs-lookup"><span data-stu-id="94876-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="94876-105">A macro do **\_ \_ quadro MCI TMSF** recupera o componente de quadros de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.</span><span class="sxs-lookup"><span data-stu-id="94876-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="94876-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94876-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="94876-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94876-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94876-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="94876-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="94876-109">Hora no formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="94876-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94876-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94876-110">Return value</span></span>

<span data-ttu-id="94876-111">Retorna o componente de quadros das informações de TMSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="94876-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="94876-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="94876-112">Remarks</span></span>

<span data-ttu-id="94876-113">O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.</span><span class="sxs-lookup"><span data-stu-id="94876-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="94876-114">A macro do **\_ \_ quadro MCI TMSF** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="94876-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="94876-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94876-115">Requirements</span></span>



| <span data-ttu-id="94876-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="94876-116">Requirement</span></span> | <span data-ttu-id="94876-117">Valor</span><span class="sxs-lookup"><span data-stu-id="94876-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94876-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94876-118">Minimum supported client</span></span><br/> | <span data-ttu-id="94876-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94876-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="94876-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94876-120">Minimum supported server</span></span><br/> | <span data-ttu-id="94876-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94876-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="94876-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94876-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="94876-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="94876-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94876-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="94876-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94876-125">MCI</span><span class="sxs-lookup"><span data-stu-id="94876-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="94876-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="94876-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





