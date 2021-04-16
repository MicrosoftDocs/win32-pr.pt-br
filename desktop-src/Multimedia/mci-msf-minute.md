---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: A macro de minuto do MSF do MCI \_ \_ recupera o componente de minutos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- Multimídia MCI_MSF_MINUTE macro do Windows
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751175"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="fad79-104">Macro de minuto do \_ MSF MCI \_</span><span class="sxs-lookup"><span data-stu-id="fad79-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="fad79-105">A macro de **\_ \_ minuto do MSF do MCI** recupera o componente de minutos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).</span><span class="sxs-lookup"><span data-stu-id="fad79-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad79-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fad79-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="fad79-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fad79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad79-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="fad79-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="fad79-109">Hora no formato MSF.</span><span class="sxs-lookup"><span data-stu-id="fad79-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad79-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fad79-110">Return value</span></span>

<span data-ttu-id="fad79-111">Retorna o componente de minutos das informações de MSF especificadas.</span><span class="sxs-lookup"><span data-stu-id="fad79-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad79-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fad79-112">Remarks</span></span>

<span data-ttu-id="fad79-113">O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros.</span><span class="sxs-lookup"><span data-stu-id="fad79-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="fad79-114">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="fad79-114">The most significant byte is unused.</span></span>

<span data-ttu-id="fad79-115">A macro de **\_ \_ minuto do MSF do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fad79-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="fad79-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fad79-116">Requirements</span></span>



| <span data-ttu-id="fad79-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad79-117">Requirement</span></span> | <span data-ttu-id="fad79-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fad79-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fad79-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fad79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fad79-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fad79-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fad79-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fad79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fad79-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fad79-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fad79-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fad79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad79-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad79-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad79-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fad79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad79-126">MCI</span><span class="sxs-lookup"><span data-stu-id="fad79-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fad79-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="fad79-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





