---
title: Macro MCI_TMSF_SECOND (Mciapi. h)
description: A \_ segunda macro do MCI TMSF \_ recupera o componente de segundos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- Multimídia MCI_TMSF_SECOND macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085665"
---
# <a name="mci_tmsf_second-macro"></a><span data-ttu-id="4f1f8-104">\_Macro da \_ segunda TMSF MCI</span><span class="sxs-lookup"><span data-stu-id="4f1f8-104">MCI\_TMSF\_SECOND macro</span></span>

<span data-ttu-id="4f1f8-105">A **\_ \_ segunda macro do MCI TMSF** recupera o componente de segundos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-105">The **MCI\_TMSF\_SECOND** macro retrieves the seconds component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1f8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1f8-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="4f1f8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1f8-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="4f1f8-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="4f1f8-109">Hora no formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1f8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f1f8-110">Return value</span></span>

<span data-ttu-id="4f1f8-111">Retorna o componente de segundos das informações de TMSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-111">Returns the seconds component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1f8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f1f8-112">Remarks</span></span>

<span data-ttu-id="4f1f8-113">O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="4f1f8-114">A **\_ \_ segunda macro TMSF do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4f1f8-114">The **MCI\_TMSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="4f1f8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f1f8-115">Requirements</span></span>



| <span data-ttu-id="4f1f8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1f8-116">Requirement</span></span> | <span data-ttu-id="4f1f8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4f1f8-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1f8-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f1f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1f8-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4f1f8-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f1f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1f8-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4f1f8-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4f1f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1f8-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f8-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f1f8-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4f1f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1f8-125">MCI</span><span class="sxs-lookup"><span data-stu-id="4f1f8-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4f1f8-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="4f1f8-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





