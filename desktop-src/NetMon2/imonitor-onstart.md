---
description: O método OnStart é um método opcional que pode ser implementado pelo monitor. O MCSVC chama esse método para solicitar que o monitor inicie a captura.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Método IMonitor:: OnStart (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089958"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="6ad31-104">Método IMonitor:: OnStart</span><span class="sxs-lookup"><span data-stu-id="6ad31-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="6ad31-105">O método **OnStart** é um método opcional que pode ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="6ad31-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="6ad31-106">O MCSVC chama esse método para solicitar que o monitor inicie a captura.</span><span class="sxs-lookup"><span data-stu-id="6ad31-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad31-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ad31-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="6ad31-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ad31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad31-109">*pUnkNPP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad31-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad31-110">Um ponteiro [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface [IRTC](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad31-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="6ad31-111">O monitor pode usar essa interface para obter estatísticas que podem ser usadas para determinar se a captura deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6ad31-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad31-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ad31-112">Return value</span></span>

<span data-ttu-id="6ad31-113">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).</span><span class="sxs-lookup"><span data-stu-id="6ad31-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="6ad31-114">Quando S \_ OK é retornado, o MCSVC chama o método [IRTC:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad31-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="6ad31-115">Se o método não for bem-sucedido, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="6ad31-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="6ad31-116">O MCSVC não iniciará a captura se qualquer código de erro for retornado.</span><span class="sxs-lookup"><span data-stu-id="6ad31-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad31-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ad31-117">Remarks</span></span>

<span data-ttu-id="6ad31-118">O MCSVC chama esse método antes de o método [IRTC:: Start](irtc-start.md) do NPP ser chamado para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="6ad31-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad31-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ad31-119">Requirements</span></span>



| <span data-ttu-id="6ad31-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad31-120">Requirement</span></span> | <span data-ttu-id="6ad31-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad31-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad31-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad31-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ad31-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6ad31-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad31-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ad31-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ad31-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ad31-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad31-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad31-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad31-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ad31-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad31-129">IMonitor</span><span class="sxs-lookup"><span data-stu-id="6ad31-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="6ad31-130">Provedores de pacotes de rede</span><span class="sxs-lookup"><span data-stu-id="6ad31-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

