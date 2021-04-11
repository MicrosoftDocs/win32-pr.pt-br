---
description: O método GetEventData aloca espaço para as estruturas NMEVENTDATA e NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Método IMonitorEventer:: GetEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164409"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="11de6-103">Método IMonitorEventer:: GetEventData</span><span class="sxs-lookup"><span data-stu-id="11de6-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="11de6-104">O método **GetEventData** aloca espaço para as estruturas [NMEVENTDATA](nmeventdata.md) e [NMCOLUMNINFO](nmcolumninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="11de6-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="11de6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11de6-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="11de6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11de6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11de6-107">*bNumColumns* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11de6-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11de6-108">Número de estruturas **NMCOLUMNINFO** necessárias.</span><span class="sxs-lookup"><span data-stu-id="11de6-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="11de6-109">*ppNMEventData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="11de6-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11de6-110">Endereço da estrutura **NMEVENTDATA** que é retornada.</span><span class="sxs-lookup"><span data-stu-id="11de6-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11de6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11de6-111">Return value</span></span>

<span data-ttu-id="11de6-112">Se o método for bem-sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11de6-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="11de6-113">Se o método não for bem-sucedido, o valor de retorno será NMERR \_ memória insuficiente \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="11de6-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="11de6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="11de6-114">Remarks</span></span>

<span data-ttu-id="11de6-115">Os monitores chamam esse método para alocar memória para os dados de evento e estruturas de informações de coluna.</span><span class="sxs-lookup"><span data-stu-id="11de6-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="11de6-116">Para liberar memória alocada para uma estrutura **NMEVENTDATA** , consulte [IMonitorEventer:: FreeEventData](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="11de6-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11de6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11de6-117">Requirements</span></span>



| <span data-ttu-id="11de6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11de6-118">Requirement</span></span> | <span data-ttu-id="11de6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="11de6-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11de6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11de6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11de6-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11de6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="11de6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11de6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11de6-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11de6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11de6-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="11de6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11de6-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="11de6-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11de6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11de6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11de6-127">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="11de6-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="11de6-128">IMonitorEventer::FreeEventData</span><span class="sxs-lookup"><span data-stu-id="11de6-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="11de6-129">NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="11de6-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="11de6-130">NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="11de6-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




