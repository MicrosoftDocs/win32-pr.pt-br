---
description: A função DllGetMonitorObject deve ser implementada pelo monitor. O MCSVC chama essa função para criar uma instância do monitor.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Função de retorno de chamada DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836991"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="7abdd-104">Função de retorno de chamada DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="7abdd-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="7abdd-105">A função **DllGetMonitorObject** deve ser implementada pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="7abdd-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="7abdd-106">O MCSVC chama essa função para criar uma instância do monitor.</span><span class="sxs-lookup"><span data-stu-id="7abdd-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abdd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7abdd-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="7abdd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7abdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abdd-109">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7abdd-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-110">UUID de monitores, mostrado abaixo, conforme definido no arquivo de cabeçalho IMonitor. h.</span><span class="sxs-lookup"><span data-stu-id="7abdd-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="7abdd-111">Se um UUID inválido for fornecido, a função falhará e o monitor deverá retornar E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="7abdd-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="7abdd-112">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7abdd-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-113">Ponteiro para um ponteiro que recebe a interface solicitada em *riid*.</span><span class="sxs-lookup"><span data-stu-id="7abdd-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abdd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7abdd-114">Return value</span></span>

<span data-ttu-id="7abdd-115">Se a função for bem-sucedida, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).</span><span class="sxs-lookup"><span data-stu-id="7abdd-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="7abdd-116">Se a função não for bem-sucedida, o valor de retorno será um código de falha.</span><span class="sxs-lookup"><span data-stu-id="7abdd-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="7abdd-117">Quando um código de falha é retornado, o MCSVC não cria o objeto monitor e o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) não é chamado no ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="7abdd-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abdd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7abdd-118">Remarks</span></span>

<span data-ttu-id="7abdd-119">A função **DllGetMonitorObject** é chamada cada vez que o MCSVC tenta criar uma instância do monitor.</span><span class="sxs-lookup"><span data-stu-id="7abdd-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="7abdd-120">Essa função possui intencionalmente uma forte semelhança com a função [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) mais comum.</span><span class="sxs-lookup"><span data-stu-id="7abdd-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="7abdd-121">A principal diferença é que um CLSID não é passado para **DllGetMonitorObject**.</span><span class="sxs-lookup"><span data-stu-id="7abdd-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abdd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abdd-122">Requirements</span></span>



| <span data-ttu-id="7abdd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abdd-123">Requirement</span></span> | <span data-ttu-id="7abdd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7abdd-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7abdd-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7abdd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7abdd-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7abdd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7abdd-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7abdd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7abdd-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7abdd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7abdd-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7abdd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7abdd-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7abdd-130"><dt>Netmon.h</dt></span></span> </dl> |



 

