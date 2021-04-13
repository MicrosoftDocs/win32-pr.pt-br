---
title: Método GetVersion do INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter a versão de um cliente de integridade.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Método GetVersion NAP
- Método GetVersion NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método GetVersion
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499831"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="6fdaf-106">Método INapComponentInfo:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="6fdaf-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="6fdaf-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="6fdaf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6fdaf-108">O método de retorno de chamada **INapComponentInfo:: GetVersion** é usado pelo sistema NAP para obter a versão de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdaf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fdaf-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="6fdaf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fdaf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fdaf-111">*versão* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6fdaf-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdaf-112">Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da versão.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fdaf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fdaf-113">Return value</span></span>

<span data-ttu-id="6fdaf-114">Retorne um desses códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="6fdaf-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6fdaf-115">Return code</span></span>                                                                                     | <span data-ttu-id="6fdaf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fdaf-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6fdaf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6fdaf-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="6fdaf-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6fdaf-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6fdaf-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6fdaf-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fdaf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fdaf-123">Requirements</span></span>



| <span data-ttu-id="6fdaf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fdaf-124">Requirement</span></span> | <span data-ttu-id="6fdaf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6fdaf-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdaf-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdaf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdaf-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fdaf-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6fdaf-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdaf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdaf-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fdaf-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6fdaf-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fdaf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fdaf-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fdaf-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="6fdaf-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fdaf-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdaf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fdaf-134">See also</span></span>

<dl> <span data-ttu-id="6fdaf-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6fdaf-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6fdaf-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="6fdaf-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





