---
description: Obtém o status atual do cartão inteligente ou leitor.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'Método ISCardManage:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749685"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="2edcd-103">Método ISCardManage:: status</span><span class="sxs-lookup"><span data-stu-id="2edcd-103">ISCardManage::Status method</span></span>

<span data-ttu-id="2edcd-104">\[O método de **status** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2edcd-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2edcd-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2edcd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2edcd-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2edcd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2edcd-107">O método de **status** Obtém o status atual do [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2edcd-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2edcd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2edcd-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="2edcd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2edcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edcd-110">*pStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2edcd-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edcd-111">Ponteiro para um valor de enumeração de Estados SCARTARs \_ .</span><span class="sxs-lookup"><span data-stu-id="2edcd-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="2edcd-112">No retorno, contém o status/estado atual.</span><span class="sxs-lookup"><span data-stu-id="2edcd-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="2edcd-113">*pProtocols* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2edcd-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edcd-114">Ponteiro para um \_ valor de enumeração de protocolos scartar.</span><span class="sxs-lookup"><span data-stu-id="2edcd-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="2edcd-115">No retorno, contém o protocolo atual.</span><span class="sxs-lookup"><span data-stu-id="2edcd-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2edcd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2edcd-116">Return value</span></span>

<span data-ttu-id="2edcd-117">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="2edcd-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="2edcd-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2edcd-118">Return code</span></span>                                                                                   | <span data-ttu-id="2edcd-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="2edcd-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2edcd-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2edcd-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2edcd-121">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2edcd-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2edcd-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2edcd-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2edcd-123">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="2edcd-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2edcd-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2edcd-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2edcd-125">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="2edcd-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="2edcd-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2edcd-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2edcd-127">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2edcd-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2edcd-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2edcd-128">Remarks</span></span>

<span data-ttu-id="2edcd-129">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="2edcd-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="2edcd-130">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2edcd-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2edcd-131">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2edcd-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2edcd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2edcd-132">Requirements</span></span>



| <span data-ttu-id="2edcd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2edcd-133">Requirement</span></span> | <span data-ttu-id="2edcd-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2edcd-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2edcd-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2edcd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2edcd-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2edcd-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2edcd-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2edcd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2edcd-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2edcd-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2edcd-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2edcd-139">End of client support</span></span><br/>    | <span data-ttu-id="2edcd-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2edcd-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2edcd-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2edcd-141">End of server support</span></span><br/>    | <span data-ttu-id="2edcd-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2edcd-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2edcd-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2edcd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edcd-144">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="2edcd-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
