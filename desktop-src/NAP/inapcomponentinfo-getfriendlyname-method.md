---
title: Método getfriendlyname do INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Método getfriendlyname NAP
- Método getfriendlyname NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método getamigávelname
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455879"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="982cc-106">Método INapComponentInfo:: getfriendlyname</span><span class="sxs-lookup"><span data-stu-id="982cc-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="982cc-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="982cc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="982cc-108">O método de retorno de chamada **INapComponentInfo:: Getamigávelname** é usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="982cc-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="982cc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="982cc-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="982cc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="982cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="982cc-111">*FriendlyName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="982cc-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="982cc-112">Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso do nome amigável.</span><span class="sxs-lookup"><span data-stu-id="982cc-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="982cc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="982cc-113">Return value</span></span>

<span data-ttu-id="982cc-114">Retorne um desses códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="982cc-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="982cc-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="982cc-115">Return code</span></span>                                                                                     | <span data-ttu-id="982cc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="982cc-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="982cc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="982cc-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="982cc-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="982cc-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="982cc-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="982cc-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="982cc-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="982cc-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="982cc-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="982cc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="982cc-123">Requirements</span></span>



| <span data-ttu-id="982cc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="982cc-124">Requirement</span></span> | <span data-ttu-id="982cc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="982cc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="982cc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="982cc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="982cc-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="982cc-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="982cc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="982cc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="982cc-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="982cc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="982cc-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="982cc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="982cc-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="982cc-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="982cc-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="982cc-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="982cc-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="982cc-134">See also</span></span>

<dl> <span data-ttu-id="982cc-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="982cc-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="982cc-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="982cc-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





