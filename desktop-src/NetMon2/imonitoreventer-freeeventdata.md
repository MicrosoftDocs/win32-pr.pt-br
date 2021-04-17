---
description: O método FreeEventData libera espaço alocado para a estrutura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Método IMonitorEventer:: FreeEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758742"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="6a2e7-103">Método IMonitorEventer:: FreeEventData</span><span class="sxs-lookup"><span data-stu-id="6a2e7-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="6a2e7-104">O método **FreeEventData** libera espaço alocado para a estrutura [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6a2e7-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a2e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a2e7-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="6a2e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a2e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a2e7-107">*pNMEventData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a2e7-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e7-108">Endereço da estrutura [**NMEVENTDATA**](nmeventdata.md) , a memória do que é liberada.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a2e7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a2e7-109">Return value</span></span>

<span data-ttu-id="6a2e7-110">Esse método retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a2e7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a2e7-111">Remarks</span></span>

<span data-ttu-id="6a2e7-112">Os monitores chamam esse método para liberar a memória que eles alocam para a estrutura de dados de evento.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="6a2e7-113">Lembre-se de que, embora o monitor ainda tenha um ponteiro para cadeias de caracteres em uma estrutura [**NMEVENTDATA**](nmeventdata.md) alocada, a memória para essas cadeias de caracteres deve ser liberada antes que o método **FreeEventData** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="6a2e7-114">Para obter mais informações sobre como alocar memória para uma estrutura [**NMEVENTDATA**](nmeventdata.md) , consulte [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="6a2e7-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a2e7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a2e7-115">Requirements</span></span>



| <span data-ttu-id="6a2e7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a2e7-116">Requirement</span></span> | <span data-ttu-id="6a2e7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6a2e7-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2e7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a2e7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a2e7-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a2e7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6a2e7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a2e7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a2e7-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a2e7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a2e7-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6a2e7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a2e7-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a2e7-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a2e7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a2e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2e7-125">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="6a2e7-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="6a2e7-126">**IMonitorEventer::GetEventData**</span><span class="sxs-lookup"><span data-stu-id="6a2e7-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="6a2e7-127">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="6a2e7-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




