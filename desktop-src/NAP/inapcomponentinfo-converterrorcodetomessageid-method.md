---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: É usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Método ConvertErrorCodeToMessageId NAP
- Método ConvertErrorCodeToMessageId NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455880"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="12fa7-106">Método INapComponentInfo:: ConvertErrorCodeToMessageId</span><span class="sxs-lookup"><span data-stu-id="12fa7-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="12fa7-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="12fa7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="12fa7-108">O método de retorno de chamada **INapComponentInfo:: ConvertErrorCodeToMessageId** é usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="12fa7-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fa7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12fa7-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="12fa7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12fa7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fa7-111">*ErrorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12fa7-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa7-112">O [**código de erro**](nap-error-constants.md) do sistema NAP que deve ser convertido em uma **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="12fa7-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="12fa7-113">*msgid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="12fa7-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa7-114">Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da cadeia de caracteres localizada correspondente.</span><span class="sxs-lookup"><span data-stu-id="12fa7-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fa7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12fa7-115">Return value</span></span>

<span data-ttu-id="12fa7-116">Retorne um desses códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="12fa7-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="12fa7-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="12fa7-117">Return code</span></span>                                                                                     | <span data-ttu-id="12fa7-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="12fa7-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="12fa7-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="12fa7-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="12fa7-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="12fa7-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="12fa7-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="12fa7-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="12fa7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="12fa7-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="12fa7-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12fa7-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="12fa7-125">Remarks</span></span>

<span data-ttu-id="12fa7-126">O **MessageId** retornado é usado pelo sistema NAP para recuperar uma cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="12fa7-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fa7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12fa7-127">Requirements</span></span>



| <span data-ttu-id="12fa7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fa7-128">Requirement</span></span> | <span data-ttu-id="12fa7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12fa7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fa7-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12fa7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12fa7-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12fa7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12fa7-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12fa7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12fa7-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12fa7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="12fa7-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12fa7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="12fa7-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="12fa7-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="12fa7-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12fa7-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fa7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="12fa7-138">See also</span></span>

<dl> <span data-ttu-id="12fa7-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="12fa7-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="12fa7-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="12fa7-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





