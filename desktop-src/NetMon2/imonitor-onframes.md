---
description: O método onframes deve ser implementado pelo monitor. O MCSVC chama esse método quando o buffer de captura está cheio ou o tempo de atualização passou.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Método IMonitor:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647046"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="5d553-104">Método IMonitor:: onframes</span><span class="sxs-lookup"><span data-stu-id="5d553-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="5d553-105">O método **Onframes** deve ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="5d553-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="5d553-106">O MCSVC chama esse método quando o buffer de captura está cheio ou o tempo de atualização passou.</span><span class="sxs-lookup"><span data-stu-id="5d553-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d553-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d553-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="5d553-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d553-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d553-109">*Evento* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5d553-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d553-110">[Atualizar \_ o ](update-event.md) Estrutura de eventos que contém informações de quadro usadas para atualizar eventos.</span><span class="sxs-lookup"><span data-stu-id="5d553-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d553-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d553-111">Return value</span></span>

<span data-ttu-id="5d553-112">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).</span><span class="sxs-lookup"><span data-stu-id="5d553-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="5d553-113">O MCSVC passa o valor retornado de volta para o NPP para processamento.</span><span class="sxs-lookup"><span data-stu-id="5d553-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="5d553-114">Se o método não for bem-sucedido, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="5d553-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="5d553-115">O MCSVC passa o valor retornado de volta para o NPP para processamento.</span><span class="sxs-lookup"><span data-stu-id="5d553-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d553-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d553-116">Requirements</span></span>



| <span data-ttu-id="5d553-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d553-117">Requirement</span></span> | <span data-ttu-id="5d553-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5d553-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d553-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d553-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d553-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d553-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5d553-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d553-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d553-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d553-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d553-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d553-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d553-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d553-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




