---
description: Libera o anexo para um determinado cartão inteligente ou leitor alocado por AttachByHandle e AttachByIFD, respectivamente.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: 'ISCardManage: método Etach de:D'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091123"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="cb4c5-103">ISCardManage: método Etach de:D</span><span class="sxs-lookup"><span data-stu-id="cb4c5-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="cb4c5-104">\[O método **Detach** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb4c5-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cb4c5-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cb4c5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cb4c5-107">O método **Detach** libera o anexo para um determinado [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md) alocado por [**AttachByHandle**](iscardmanage-attachbyhandle.md) e [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4c5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb4c5-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="cb4c5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb4c5-109">Parameters</span></span>

<span data-ttu-id="cb4c5-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb4c5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb4c5-111">Return value</span></span>

<span data-ttu-id="cb4c5-112">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="cb4c5-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="cb4c5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cb4c5-113">Return code</span></span>                                                                                   | <span data-ttu-id="cb4c5-114">Description</span><span class="sxs-lookup"><span data-stu-id="cb4c5-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cb4c5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb4c5-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cb4c5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cb4c5-118">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="cb4c5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb4c5-119">Remarks</span></span>

<span data-ttu-id="cb4c5-120">Para anexar uma chamada de cartão inteligente [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="cb4c5-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="cb4c5-121">Para se reconectar com o cartão inteligente sem chamar **Detach** e [**AttachByHandle**](iscardmanage-attachbyhandle.md), chame [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="cb4c5-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="cb4c5-122">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="cb4c5-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="cb4c5-123">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cb4c5-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cb4c5-124">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cb4c5-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4c5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb4c5-125">Requirements</span></span>



| <span data-ttu-id="cb4c5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4c5-126">Requirement</span></span> | <span data-ttu-id="cb4c5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cb4c5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb4c5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb4c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4c5-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cb4c5-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cb4c5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb4c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4c5-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb4c5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cb4c5-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cb4c5-132">End of client support</span></span><br/>    | <span data-ttu-id="cb4c5-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb4c5-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="cb4c5-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="cb4c5-134">End of server support</span></span><br/>    | <span data-ttu-id="cb4c5-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb4c5-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="cb4c5-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb4c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4c5-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="cb4c5-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="cb4c5-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="cb4c5-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="cb4c5-139">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="cb4c5-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="cb4c5-140">**Reconectar**</span><span class="sxs-lookup"><span data-stu-id="cb4c5-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
