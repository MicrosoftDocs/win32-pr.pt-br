---
description: Cria um link de comunicação para um leitor, usando um nome de exibição fornecido para o leitor.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Método ISCardManage:: AttachByIFD'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749480"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="02c88-103">Método ISCardManage:: AttachByIFD</span><span class="sxs-lookup"><span data-stu-id="02c88-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="02c88-104">\[O método **AttachByIFD** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="02c88-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="02c88-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="02c88-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02c88-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="02c88-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="02c88-107">O método **AttachByIFD** cria um link de comunicação para um [*leitor*](../secgloss/r-gly.md), usando um nome de exibição fornecido para o leitor.</span><span class="sxs-lookup"><span data-stu-id="02c88-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c88-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02c88-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="02c88-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02c88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c88-110">*bstrIFDName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02c88-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c88-111">O nome de exibição do leitor.</span><span class="sxs-lookup"><span data-stu-id="02c88-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c88-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02c88-112">Return value</span></span>

<span data-ttu-id="02c88-113">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="02c88-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="02c88-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="02c88-114">Return code</span></span>                                                                                   | <span data-ttu-id="02c88-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="02c88-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="02c88-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02c88-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="02c88-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="02c88-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="02c88-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="02c88-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="02c88-119">O parâmetro *bstrIFDName* não é válido.</span><span class="sxs-lookup"><span data-stu-id="02c88-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="02c88-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="02c88-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="02c88-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="02c88-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="02c88-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="02c88-122">Remarks</span></span>

<span data-ttu-id="02c88-123">Para anexar uma chamada de [*cartão inteligente*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span><span class="sxs-lookup"><span data-stu-id="02c88-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="02c88-124">Para liberar uma chamada de anexo, [**desanexar**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="02c88-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="02c88-125">Para se reconectar com o cartão inteligente sem chamar [**Detach**](iscardmanage-detach.md) e **AttachByIFD**, chame [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="02c88-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="02c88-126">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="02c88-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="02c88-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="02c88-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="02c88-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="02c88-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02c88-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c88-129">Requirements</span></span>



| <span data-ttu-id="02c88-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c88-130">Requirement</span></span> | <span data-ttu-id="02c88-131">Valor</span><span class="sxs-lookup"><span data-stu-id="02c88-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02c88-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02c88-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02c88-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02c88-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="02c88-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02c88-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02c88-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02c88-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02c88-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="02c88-136">End of client support</span></span><br/>    | <span data-ttu-id="02c88-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="02c88-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="02c88-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="02c88-138">End of server support</span></span><br/>    | <span data-ttu-id="02c88-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02c88-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="02c88-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="02c88-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c88-141">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="02c88-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="02c88-142">**Detach**</span><span class="sxs-lookup"><span data-stu-id="02c88-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="02c88-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="02c88-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="02c88-144">**Reconectar**</span><span class="sxs-lookup"><span data-stu-id="02c88-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
