---
description: O método SendNMEvent envia eventos para Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Método IMonitorEventer:: SendNMEvent (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754316"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="ded15-103">Método IMonitorEventer:: SendNMEvent</span><span class="sxs-lookup"><span data-stu-id="ded15-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="ded15-104">O método **SendNMEvent** envia eventos para instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ded15-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="ded15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ded15-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="ded15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ded15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded15-107">*pNMEventData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded15-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded15-108">Ponteiro para o evento enviado ao WMI.</span><span class="sxs-lookup"><span data-stu-id="ded15-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded15-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ded15-109">Return value</span></span>

<span data-ttu-id="ded15-110">Se o método for bem-sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ded15-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="ded15-111">Se o método não for bem-sucedido, o valor de retorno será NMERR \_ memória insuficiente \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ded15-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded15-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded15-112">Requirements</span></span>



| <span data-ttu-id="ded15-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded15-113">Requirement</span></span> | <span data-ttu-id="ded15-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ded15-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ded15-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ded15-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ded15-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ded15-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ded15-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ded15-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ded15-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ded15-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ded15-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ded15-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded15-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded15-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




