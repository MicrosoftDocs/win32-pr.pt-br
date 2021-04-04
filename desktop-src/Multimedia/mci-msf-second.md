---
title: Macro MCI_MSF_SECOND (Mciapi. h)
description: A \_ segunda macro MCI do MSF \_ recupera o componente de segundos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- Multimídia MCI_MSF_SECOND macro do Windows
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824498"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="a0a4b-104">\_Segunda macro do MSF MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0a4b-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="a0a4b-105">A **\_ \_ segunda macro MCI do MSF** recupera o componente de segundos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).</span><span class="sxs-lookup"><span data-stu-id="a0a4b-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a4b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0a4b-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="a0a4b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0a4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a4b-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="a0a4b-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="a0a4b-109">Hora no formato MSF.</span><span class="sxs-lookup"><span data-stu-id="a0a4b-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a4b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0a4b-110">Return value</span></span>

<span data-ttu-id="a0a4b-111">Retorna o componente de segundos das informações de MSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="a0a4b-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a4b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0a4b-112">Remarks</span></span>

<span data-ttu-id="a0a4b-113">O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros.</span><span class="sxs-lookup"><span data-stu-id="a0a4b-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="a0a4b-114">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="a0a4b-114">The most significant byte is unused.</span></span>

<span data-ttu-id="a0a4b-115">A **\_ \_ segunda macro do MSF MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a0a4b-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="a0a4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a4b-116">Requirements</span></span>



| <span data-ttu-id="a0a4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a4b-117">Requirement</span></span> | <span data-ttu-id="a0a4b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a0a4b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a4b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a4b-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a4b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0a4b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a4b-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a4b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0a4b-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0a4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0a4b-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a4b-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a4b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0a4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a4b-126">MCI</span><span class="sxs-lookup"><span data-stu-id="a0a4b-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a0a4b-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="a0a4b-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





