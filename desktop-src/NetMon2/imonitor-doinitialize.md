---
description: O método doinitialize deve ser implementado pelo monitor. O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método NPPs IRTCConnect.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501343"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="4823d-104">IMonitor: método oInitialize de:D</span><span class="sxs-lookup"><span data-stu-id="4823d-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="4823d-105">O método **doinitialize** deve ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="4823d-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="4823d-106">O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método [IRTC:: Connect](irtc-connect.md) do NPP.</span><span class="sxs-lookup"><span data-stu-id="4823d-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4823d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4823d-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4823d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4823d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4823d-109">*pUnkMonitorCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4823d-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4823d-110">Um ponteiro [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passado pelo MCSVC.</span><span class="sxs-lookup"><span data-stu-id="4823d-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="4823d-111">Para obter uma interface de controle de monitor com suporte, o monitor deve chamar [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4823d-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="4823d-112">*hNPPBlob* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4823d-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4823d-113">Na entrada, um identificador para um BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="4823d-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="4823d-114">Na saída, um BLOB NPP que contém um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="4823d-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4823d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4823d-115">Return value</span></span>

<span data-ttu-id="4823d-116">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).</span><span class="sxs-lookup"><span data-stu-id="4823d-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="4823d-117">Se o método não for bem-sucedido, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="4823d-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="4823d-118">Se houver erro, o MCSVC não criará o monitor ou chamará [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="4823d-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="4823d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4823d-119">Remarks</span></span>

<span data-ttu-id="4823d-120">O MCSVC chama o método **doinitialize** para executar qualquer inicialização de monitor necessária.</span><span class="sxs-lookup"><span data-stu-id="4823d-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="4823d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4823d-121">Requirements</span></span>



| <span data-ttu-id="4823d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4823d-122">Requirement</span></span> | <span data-ttu-id="4823d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4823d-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4823d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4823d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4823d-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4823d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4823d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4823d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4823d-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4823d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4823d-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4823d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4823d-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4823d-129"><dt>Netmon.h</dt></span></span> </dl> |



 

