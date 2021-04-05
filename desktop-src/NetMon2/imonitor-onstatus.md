---
description: O método MCSVC chama o método OnStatus para notificar o monitor de que existe um evento de status NPP. Esse método deve ser implementado pelo monitor.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Método IMonitor:: OnStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090927"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="217b7-104">Método IMonitor:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="217b7-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="217b7-105">O método MCSVC chama o método **OnStatus** para notificar o monitor de que existe um evento de status NPP.</span><span class="sxs-lookup"><span data-stu-id="217b7-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="217b7-106">Esse método deve ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="217b7-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="217b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="217b7-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="217b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="217b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217b7-109">*Evento* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="217b7-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217b7-110">Uma estrutura de [ \_ eventos de atualização](update-event.md) .</span><span class="sxs-lookup"><span data-stu-id="217b7-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217b7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="217b7-111">Return value</span></span>

<span data-ttu-id="217b7-112">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR) e o MCSVC passará o valor retornado de volta para o NPP para processamento.</span><span class="sxs-lookup"><span data-stu-id="217b7-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="217b7-113">Se o método não for bem-sucedido, retorne um código de erro.</span><span class="sxs-lookup"><span data-stu-id="217b7-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="217b7-114">Se houver erro, o MCSVC passa o valor retornado de volta para o NPP para processamento.</span><span class="sxs-lookup"><span data-stu-id="217b7-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="217b7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="217b7-115">Requirements</span></span>



| <span data-ttu-id="217b7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="217b7-116">Requirement</span></span> | <span data-ttu-id="217b7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="217b7-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="217b7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="217b7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="217b7-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="217b7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="217b7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="217b7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="217b7-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="217b7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="217b7-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="217b7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="217b7-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="217b7-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




