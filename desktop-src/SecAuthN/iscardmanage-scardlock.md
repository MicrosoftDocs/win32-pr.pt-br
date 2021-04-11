---
description: Bloqueia um cartão inteligente conectado para uso exclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Método ISCardManage:: SCardLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165344"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="6433a-103">Método ISCardManage:: SCardLock</span><span class="sxs-lookup"><span data-stu-id="6433a-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="6433a-104">\[O método **SCardLock** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6433a-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6433a-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6433a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6433a-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6433a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6433a-107">O método **SCardLock** bloqueia um [*cartão inteligente*](../secgloss/s-gly.md) conectado para uso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6433a-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="6433a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6433a-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="6433a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6433a-109">Parameters</span></span>

<span data-ttu-id="6433a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6433a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6433a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6433a-111">Return value</span></span>

<span data-ttu-id="6433a-112">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="6433a-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="6433a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6433a-113">Return code</span></span>                                                                            | <span data-ttu-id="6433a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6433a-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6433a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6433a-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6433a-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6433a-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6433a-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="6433a-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6433a-118">Falha ao concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6433a-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6433a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6433a-119">Remarks</span></span>

<span data-ttu-id="6433a-120">Para liberar o uso exclusivo do cartão inteligente conectado, chame [**SCardUnlock**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="6433a-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="6433a-121">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="6433a-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="6433a-122">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6433a-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6433a-123">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6433a-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6433a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6433a-124">Requirements</span></span>



| <span data-ttu-id="6433a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6433a-125">Requirement</span></span> | <span data-ttu-id="6433a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6433a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6433a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6433a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6433a-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6433a-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6433a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6433a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6433a-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6433a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6433a-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6433a-131">End of client support</span></span><br/>    | <span data-ttu-id="6433a-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6433a-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6433a-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6433a-133">End of server support</span></span><br/>    | <span data-ttu-id="6433a-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6433a-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6433a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6433a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6433a-136">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="6433a-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="6433a-137">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="6433a-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
