---
description: Libera o uso exclusivo do cartão inteligente conectado.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Método ISCardManage:: SCardUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165342"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="2f2ef-103">Método ISCardManage:: SCardUnlock</span><span class="sxs-lookup"><span data-stu-id="2f2ef-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="2f2ef-104">\[O método **SCardUnlock** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f2ef-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f2ef-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2f2ef-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2f2ef-107">O método **SCardUnlock** libera o uso exclusivo do [*cartão inteligente*](../secgloss/s-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2ef-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f2ef-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="2f2ef-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f2ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2ef-110">*Disposição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2f2ef-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2ef-111">O estado para sair do cartão inteligente quando o bloqueio é liberado.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="2f2ef-112">**Deixe**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="2f2ef-113">**REDEFINIR**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="2f2ef-114">**Desligamento**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="2f2ef-115">**EJEÇÃO**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2ef-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f2ef-116">Return value</span></span>

<span data-ttu-id="2f2ef-117">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2f2ef-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f2ef-118">Return code</span></span>                                                                                  | <span data-ttu-id="2f2ef-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f2ef-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2f2ef-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ef-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2f2ef-121">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="2f2ef-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ef-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2f2ef-123">O parâmetro de *disposição* não é válido.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f2ef-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f2ef-124">Remarks</span></span>

<span data-ttu-id="2f2ef-125">Para bloquear o cartão inteligente conectado, chame [**SCardLock**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="2f2ef-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="2f2ef-126">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="2f2ef-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="2f2ef-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2f2ef-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2f2ef-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2f2ef-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2ef-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f2ef-129">Requirements</span></span>



| <span data-ttu-id="2f2ef-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2ef-130">Requirement</span></span> | <span data-ttu-id="2f2ef-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2f2ef-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f2ef-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f2ef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2ef-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f2ef-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2f2ef-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f2ef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2ef-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f2ef-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f2ef-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2f2ef-136">End of client support</span></span><br/>    | <span data-ttu-id="2f2ef-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f2ef-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2f2ef-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2f2ef-138">End of server support</span></span><br/>    | <span data-ttu-id="2f2ef-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f2ef-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2f2ef-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f2ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2ef-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="2f2ef-142">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="2f2ef-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
