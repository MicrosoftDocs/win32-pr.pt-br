---
title: Macro MCI_TMSF_TRACK (Mciapi. h)
description: A \_ macro do controle MCI TMSF \_ recupera o componente trilhas de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- Multimídia MCI_TMSF_TRACK macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824470"
---
# <a name="mci_tmsf_track-macro"></a><span data-ttu-id="76cfa-104">\_Macro de \_ controle MCI TMSF</span><span class="sxs-lookup"><span data-stu-id="76cfa-104">MCI\_TMSF\_TRACK macro</span></span>

<span data-ttu-id="76cfa-105">A macro do **\_ \_ controle MCI TMSF** recupera o componente trilhas de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.</span><span class="sxs-lookup"><span data-stu-id="76cfa-105">The **MCI\_TMSF\_TRACK** macro retrieves the tracks component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="76cfa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76cfa-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="76cfa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76cfa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76cfa-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="76cfa-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="76cfa-109">Hora no formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="76cfa-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76cfa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76cfa-110">Return value</span></span>

<span data-ttu-id="76cfa-111">Retorna o componente de trilhas das informações de TMSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="76cfa-111">Returns the tracks component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="76cfa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="76cfa-112">Remarks</span></span>

<span data-ttu-id="76cfa-113">O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.</span><span class="sxs-lookup"><span data-stu-id="76cfa-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="76cfa-114">A macro do **\_ \_ controle MCI TMSF** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="76cfa-114">The **MCI\_TMSF\_TRACK** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a><span data-ttu-id="76cfa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76cfa-115">Requirements</span></span>



| <span data-ttu-id="76cfa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="76cfa-116">Requirement</span></span> | <span data-ttu-id="76cfa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="76cfa-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="76cfa-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76cfa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76cfa-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76cfa-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="76cfa-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76cfa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76cfa-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76cfa-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="76cfa-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76cfa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76cfa-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76cfa-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76cfa-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="76cfa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76cfa-125">MCI</span><span class="sxs-lookup"><span data-stu-id="76cfa-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="76cfa-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="76cfa-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





