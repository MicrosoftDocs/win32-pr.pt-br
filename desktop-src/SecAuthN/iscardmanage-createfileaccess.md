---
description: Cria uma interface ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'Método ISCardManage:: createfileaccess'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751821"
---
# <a name="iscardmanagecreatefileaccess-method"></a><span data-ttu-id="5e419-103">Método ISCardManage:: createfileaccess</span><span class="sxs-lookup"><span data-stu-id="5e419-103">ISCardManage::CreateFileAccess method</span></span>

<span data-ttu-id="5e419-104">\[O método **createfileaccess** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5e419-104">\[The **CreateFileAccess** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5e419-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5e419-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5e419-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5e419-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5e419-107">O método **createfileaccess** cria uma interface [**ISCardFileAccess**](iscardfileaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="5e419-107">The **CreateFileAccess** method creates an [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e419-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e419-108">Syntax</span></span>


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a><span data-ttu-id="5e419-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e419-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e419-110">*ppISCardFileAccess* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5e419-110">*ppISCardFileAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e419-111">Ponteiro retornado para a interface [**ISCardFileAccess**](iscardfileaccess.md) criada.</span><span class="sxs-lookup"><span data-stu-id="5e419-111">Returned pointer to the created [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e419-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e419-112">Return value</span></span>

<span data-ttu-id="5e419-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="5e419-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5e419-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5e419-114">Return code</span></span>                                                                                   | <span data-ttu-id="5e419-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e419-115">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="5e419-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e419-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5e419-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5e419-117">Operation completed successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="5e419-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5e419-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5e419-119">O parâmetro *ppISCardFileAccess* não é válido.</span><span class="sxs-lookup"><span data-stu-id="5e419-119">The *ppISCardFileAccess* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="5e419-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5e419-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5e419-121">Um ponteiro inadequado foi passado em *ppISCardFileAccess*.</span><span class="sxs-lookup"><span data-stu-id="5e419-121">A bad pointer was passed in *ppISCardFileAccess*.</span></span><br/> |
| <dl> <span data-ttu-id="5e419-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5e419-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5e419-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="5e419-123">Out of memory.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="5e419-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e419-124">Remarks</span></span>

<span data-ttu-id="5e419-125">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="5e419-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="5e419-126">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5e419-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5e419-127">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5e419-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e419-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e419-128">Requirements</span></span>



| <span data-ttu-id="5e419-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e419-129">Requirement</span></span> | <span data-ttu-id="5e419-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5e419-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e419-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e419-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5e419-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5e419-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5e419-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e419-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5e419-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e419-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5e419-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5e419-135">End of client support</span></span><br/>    | <span data-ttu-id="5e419-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e419-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="5e419-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5e419-137">End of server support</span></span><br/>    | <span data-ttu-id="5e419-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e419-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="5e419-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e419-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e419-140">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="5e419-140">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="5e419-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="5e419-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
