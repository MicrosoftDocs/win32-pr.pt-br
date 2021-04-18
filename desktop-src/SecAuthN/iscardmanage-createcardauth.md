---
description: Cria uma interface ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'Método ISCardManage:: CreateCardAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749763"
---
# <a name="iscardmanagecreatecardauth-method"></a><span data-ttu-id="e4fce-103">Método ISCardManage:: CreateCardAuth</span><span class="sxs-lookup"><span data-stu-id="e4fce-103">ISCardManage::CreateCardAuth method</span></span>

<span data-ttu-id="e4fce-104">\[O método **CreateCardAuth** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e4fce-104">\[The **CreateCardAuth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e4fce-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e4fce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4fce-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e4fce-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e4fce-107">O método **CreateCardAuth** cria uma interface [**ISCardAuth**](iscardauth.md) .</span><span class="sxs-lookup"><span data-stu-id="e4fce-107">The **CreateCardAuth** method creates an [**ISCardAuth**](iscardauth.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fce-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4fce-108">Syntax</span></span>


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a><span data-ttu-id="e4fce-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4fce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fce-110">*ppISCardAuth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4fce-110">*ppISCardAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fce-111">Ponteiro retornado para a interface criada.</span><span class="sxs-lookup"><span data-stu-id="e4fce-111">Returned pointer to the created interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fce-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4fce-112">Return value</span></span>

<span data-ttu-id="e4fce-113">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="e4fce-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="e4fce-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e4fce-114">Return code</span></span>                                                                                   | <span data-ttu-id="e4fce-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4fce-115">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="e4fce-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fce-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4fce-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e4fce-117">Operation completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="e4fce-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fce-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e4fce-119">O parâmetro *ppISCardAuth* não é válido.</span><span class="sxs-lookup"><span data-stu-id="e4fce-119">The *ppISCardAuth* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="e4fce-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fce-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4fce-121">Um ponteiro inadequado foi passado em *ppISCardAuth*.</span><span class="sxs-lookup"><span data-stu-id="e4fce-121">A bad pointer was passed in *ppISCardAuth*.</span></span><br/> |
| <dl> <span data-ttu-id="e4fce-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fce-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e4fce-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="e4fce-123">Out of memory.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="e4fce-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4fce-124">Remarks</span></span>

<span data-ttu-id="e4fce-125">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="e4fce-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="e4fce-126">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e4fce-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e4fce-127">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e4fce-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fce-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4fce-128">Requirements</span></span>



| <span data-ttu-id="e4fce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4fce-129">Requirement</span></span> | <span data-ttu-id="e4fce-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e4fce-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4fce-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4fce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fce-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e4fce-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e4fce-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4fce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fce-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4fce-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e4fce-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e4fce-135">End of client support</span></span><br/>    | <span data-ttu-id="e4fce-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4fce-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="e4fce-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e4fce-137">End of server support</span></span><br/>    | <span data-ttu-id="e4fce-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4fce-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e4fce-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4fce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fce-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="e4fce-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
