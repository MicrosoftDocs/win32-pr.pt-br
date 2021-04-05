---
description: Redefine o contexto de segurança atual do cartão inteligente.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'Método ISCardVerify:: ResetSecurityState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826819"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="4b73e-103">Método ISCardVerify:: ResetSecurityState</span><span class="sxs-lookup"><span data-stu-id="4b73e-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="4b73e-104">\[O método **ResetSecurityState** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4b73e-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b73e-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b73e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b73e-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4b73e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4b73e-107">O método **ResetSecurityState** redefine o [*contexto de segurança*](../secgloss/s-gly.md) atual do [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4b73e-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b73e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b73e-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="4b73e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b73e-109">Parameters</span></span>

<span data-ttu-id="4b73e-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b73e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b73e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b73e-111">Return value</span></span>

<span data-ttu-id="4b73e-112">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="4b73e-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="4b73e-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b73e-113">Return code</span></span>                                                                                   | <span data-ttu-id="4b73e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b73e-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4b73e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b73e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4b73e-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4b73e-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4b73e-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4b73e-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4b73e-118">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4b73e-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4b73e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b73e-119">Remarks</span></span>

<span data-ttu-id="4b73e-120">Para reabilitar o [*contexto de segurança*](../secgloss/s-gly.md) sem redefinir, chame [**desbloquear**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4b73e-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="4b73e-121">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="4b73e-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="4b73e-122">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4b73e-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4b73e-123">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4b73e-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b73e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b73e-124">Requirements</span></span>



| <span data-ttu-id="4b73e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b73e-125">Requirement</span></span> | <span data-ttu-id="4b73e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4b73e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b73e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b73e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b73e-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b73e-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4b73e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b73e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b73e-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b73e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b73e-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4b73e-131">End of client support</span></span><br/>    | <span data-ttu-id="4b73e-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b73e-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4b73e-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4b73e-133">End of server support</span></span><br/>    | <span data-ttu-id="4b73e-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b73e-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4b73e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b73e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b73e-136">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="4b73e-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="4b73e-137">[**Bloqueá**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b73e-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
