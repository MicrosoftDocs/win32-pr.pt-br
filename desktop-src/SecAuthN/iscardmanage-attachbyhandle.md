---
description: Cria um link de comunicação para um cartão inteligente (ICC) usando um identificador retornado pelo Gerenciador de recursos de cartão inteligente.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Método ISCardManage:: AttachByHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828836"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="30c3c-103">Método ISCardManage:: AttachByHandle</span><span class="sxs-lookup"><span data-stu-id="30c3c-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="30c3c-104">\[O método **AttachByHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="30c3c-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30c3c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="30c3c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30c3c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="30c3c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="30c3c-107">O método **AttachByHandle** cria um link de comunicação para um [*cartão inteligente*](../secgloss/s-gly.md) (ICC) usando um identificador retornado pelo Gerenciador de [*recursos*](../secgloss/r-gly.md)de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="30c3c-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30c3c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30c3c-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="30c3c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30c3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c3c-110">*hICC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30c3c-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c3c-111">Um identificador para um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="30c3c-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c3c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30c3c-112">Return value</span></span>

<span data-ttu-id="30c3c-113">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="30c3c-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="30c3c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30c3c-114">Return code</span></span>                                                                                   | <span data-ttu-id="30c3c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="30c3c-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="30c3c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30c3c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30c3c-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="30c3c-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="30c3c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30c3c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="30c3c-119">O parâmetro *hICC* não é válido.</span><span class="sxs-lookup"><span data-stu-id="30c3c-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="30c3c-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="30c3c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30c3c-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="30c3c-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="30c3c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="30c3c-122">Remarks</span></span>

<span data-ttu-id="30c3c-123">Para anexar uma chamada de [*leitor*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="30c3c-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="30c3c-124">Para liberar uma chamada de anexo, [**desanexar**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="30c3c-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="30c3c-125">Para se reconectar com o cartão inteligente sem chamar [**Detach**](iscardmanage-detach.md) e **AttachByHandle**, chame [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="30c3c-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="30c3c-126">Para obter uma lista de todos os métodos definidos pela interface [**ISCardManage**](iscardmanage.md) , consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="30c3c-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="30c3c-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="30c3c-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="30c3c-128">Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="30c3c-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30c3c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30c3c-129">Requirements</span></span>



| <span data-ttu-id="30c3c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c3c-130">Requirement</span></span> | <span data-ttu-id="30c3c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="30c3c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30c3c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c3c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="30c3c-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="30c3c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="30c3c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c3c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="30c3c-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30c3c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="30c3c-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="30c3c-136">End of client support</span></span><br/>    | <span data-ttu-id="30c3c-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30c3c-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="30c3c-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="30c3c-138">End of server support</span></span><br/>    | <span data-ttu-id="30c3c-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30c3c-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="30c3c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="30c3c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c3c-141">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="30c3c-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="30c3c-142">**Detach**</span><span class="sxs-lookup"><span data-stu-id="30c3c-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="30c3c-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="30c3c-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="30c3c-144">**Reconectar**</span><span class="sxs-lookup"><span data-stu-id="30c3c-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
