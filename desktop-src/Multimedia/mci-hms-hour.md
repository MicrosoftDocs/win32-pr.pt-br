---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: A \_ macro HMS de hora do MCI \_ recupera o componente de horas de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- Multimídia MCI_HMS_HOUR macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009747"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="5c047-104">\_Macro de \_ hora HMS MCI</span><span class="sxs-lookup"><span data-stu-id="5c047-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="5c047-105">A **macro \_ HMS de \_ hora do MCI** recupera o componente de horas de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.</span><span class="sxs-lookup"><span data-stu-id="5c047-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c047-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c047-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="5c047-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c047-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c047-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="5c047-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="5c047-109">Hora no formato HMS.</span><span class="sxs-lookup"><span data-stu-id="5c047-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c047-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c047-110">Return value</span></span>

<span data-ttu-id="5c047-111">Retorna o componente de horas das informações de HMS especificadas.</span><span class="sxs-lookup"><span data-stu-id="5c047-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c047-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c047-112">Remarks</span></span>

<span data-ttu-id="5c047-113">O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos.</span><span class="sxs-lookup"><span data-stu-id="5c047-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="5c047-114">O byte mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="5c047-114">The most significant byte is unused.</span></span>

<span data-ttu-id="5c047-115">A **macro \_ HMS de \_ hora do MCI** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5c047-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="5c047-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c047-116">Requirements</span></span>



| <span data-ttu-id="5c047-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c047-117">Requirement</span></span> | <span data-ttu-id="5c047-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5c047-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c047-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c047-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c047-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c047-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c047-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c047-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c047-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c047-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c047-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c047-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c047-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c047-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c047-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c047-126">MCI</span><span class="sxs-lookup"><span data-stu-id="5c047-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5c047-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="5c047-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





