---
description: Cria a interface especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Método ISCardManage:: createinterface'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170818"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="93808-103">Método ISCardManage:: createinterface</span><span class="sxs-lookup"><span data-stu-id="93808-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="93808-104">\[O método **createinterface** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="93808-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93808-105">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="93808-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="93808-106">O método **createinterface** cria a interface especificada.</span><span class="sxs-lookup"><span data-stu-id="93808-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="93808-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93808-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="93808-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93808-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93808-109">*pguidInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93808-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93808-110">O valor de GUID da interface a ser criada.</span><span class="sxs-lookup"><span data-stu-id="93808-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="93808-111">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93808-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93808-112">O nome da interface a ser criada se o GUID não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="93808-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="93808-113">Os valores padrão são "CryptoProvider".</span><span class="sxs-lookup"><span data-stu-id="93808-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="93808-114">*pUserData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93808-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93808-115">Ponteiro para dados específicos do usuário a serem usados na criação de uma interface.</span><span class="sxs-lookup"><span data-stu-id="93808-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="93808-116">*ppInterface* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="93808-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93808-117">Ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="93808-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93808-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93808-118">Return value</span></span>

<span data-ttu-id="93808-119">Os possíveis valores de retorno são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="93808-119">The possible return values are the following:</span></span>



| <span data-ttu-id="93808-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="93808-120">Return code</span></span>                                                                                   | <span data-ttu-id="93808-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="93808-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93808-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93808-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="93808-123">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="93808-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="93808-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="93808-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="93808-125">Um dos parâmetros fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="93808-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="93808-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="93808-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="93808-127">Um ponteiro inadequado foi passado no parâmetro *pguidInterface* ou *pUserData* .</span><span class="sxs-lookup"><span data-stu-id="93808-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="93808-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="93808-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="93808-129">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="93808-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="93808-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="93808-130">Remarks</span></span>

<span data-ttu-id="93808-131">Para obter uma lista de todos os métodos definidos pela interface [**ISCardManage**](iscardmanage.md) , consulte **ISCardManage**.</span><span class="sxs-lookup"><span data-stu-id="93808-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="93808-132">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="93808-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="93808-133">Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="93808-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93808-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93808-134">Requirements</span></span>



| <span data-ttu-id="93808-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="93808-135">Requirement</span></span> | <span data-ttu-id="93808-136">Valor</span><span class="sxs-lookup"><span data-stu-id="93808-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93808-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93808-137">Minimum supported client</span></span><br/> | <span data-ttu-id="93808-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93808-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="93808-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93808-139">Minimum supported server</span></span><br/> | <span data-ttu-id="93808-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93808-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93808-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="93808-141">End of client support</span></span><br/>    | <span data-ttu-id="93808-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="93808-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="93808-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="93808-143">End of server support</span></span><br/>    | <span data-ttu-id="93808-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93808-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="93808-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="93808-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93808-146">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="93808-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
