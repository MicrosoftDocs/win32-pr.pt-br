---
description: O método OnStop deve ser implementado pelo monitor. O MSCVC chama esse método para notificar o monitor de que a captura será interrompida.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Método IMonitor:: OnStop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759358"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="174d1-104">Método IMonitor:: OnStop</span><span class="sxs-lookup"><span data-stu-id="174d1-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="174d1-105">O método **OnStop** deve ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="174d1-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="174d1-106">O MSCVC chama esse método para notificar o monitor de que a captura será interrompida.</span><span class="sxs-lookup"><span data-stu-id="174d1-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="174d1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="174d1-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="174d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="174d1-108">Parameters</span></span>

<span data-ttu-id="174d1-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="174d1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="174d1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="174d1-110">Return value</span></span>

<span data-ttu-id="174d1-111">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).</span><span class="sxs-lookup"><span data-stu-id="174d1-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="174d1-112">Se o método não for bem-sucedido, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="174d1-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="174d1-113">Quando um código de erro é retornado, o monitor não pode ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="174d1-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="174d1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="174d1-114">Remarks</span></span>

<span data-ttu-id="174d1-115">O MCSVC chama esse método após [IRTC:: Stop](irtc-stop.md) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="174d1-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="174d1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="174d1-116">Requirements</span></span>



| <span data-ttu-id="174d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="174d1-117">Requirement</span></span> | <span data-ttu-id="174d1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="174d1-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="174d1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="174d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="174d1-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="174d1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="174d1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="174d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="174d1-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="174d1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="174d1-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="174d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="174d1-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="174d1-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




