---
description: Permite que um aplicativo se reconecte a um cartão inteligente ou leitor sem a necessidade de emitir uma chamada de desanexação seguida por uma chamada AttachByHandle ou AttachByIFD, respectivamente.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Método ISCardManage:: Reconnect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827853"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="905ef-103">Método ISCardManage:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="905ef-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="905ef-104">\[O método **reconnect** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="905ef-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="905ef-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="905ef-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="905ef-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="905ef-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="905ef-107">O método **reconnect** permite que um aplicativo se reconecte a um [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md) sem a necessidade de emitir uma chamada de [**desanexação**](iscardmanage-detach.md) seguida por uma chamada [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="905ef-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="905ef-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="905ef-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="905ef-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="905ef-109">Parameters</span></span>

<span data-ttu-id="905ef-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="905ef-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="905ef-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="905ef-111">Return value</span></span>

<span data-ttu-id="905ef-112">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="905ef-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="905ef-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="905ef-113">Return code</span></span>                                                                                   | <span data-ttu-id="905ef-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="905ef-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="905ef-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="905ef-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="905ef-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="905ef-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="905ef-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="905ef-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="905ef-118">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="905ef-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="905ef-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="905ef-119">Remarks</span></span>

<span data-ttu-id="905ef-120">Para anexar uma chamada de cartão inteligente [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="905ef-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="905ef-121">Para desanexar um cartão inteligente, [**desanexe**](iscardmanage-detach.md)a chamada.</span><span class="sxs-lookup"><span data-stu-id="905ef-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="905ef-122">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="905ef-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="905ef-123">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="905ef-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="905ef-124">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="905ef-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="905ef-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="905ef-125">Requirements</span></span>



| <span data-ttu-id="905ef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="905ef-126">Requirement</span></span> | <span data-ttu-id="905ef-127">Valor</span><span class="sxs-lookup"><span data-stu-id="905ef-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="905ef-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="905ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="905ef-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="905ef-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="905ef-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="905ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="905ef-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="905ef-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="905ef-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="905ef-132">End of client support</span></span><br/>    | <span data-ttu-id="905ef-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="905ef-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="905ef-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="905ef-134">End of server support</span></span><br/>    | <span data-ttu-id="905ef-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="905ef-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="905ef-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="905ef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905ef-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="905ef-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="905ef-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="905ef-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="905ef-139">**Detach**</span><span class="sxs-lookup"><span data-stu-id="905ef-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="905ef-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="905ef-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
