---
title: Método INapComponentConfig3 DeleteConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Método DeleteConfig NAP
- Método DeleteConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644511"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="36a8c-106">INapComponentConfig3: método eleteConfig de:D</span><span class="sxs-lookup"><span data-stu-id="36a8c-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="36a8c-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="36a8c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="36a8c-108">O método **DeleteConfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="36a8c-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="36a8c-109">A ID pode ser reutilizada depois que os dados de configuração forem excluídos.</span><span class="sxs-lookup"><span data-stu-id="36a8c-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a8c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36a8c-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="36a8c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36a8c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a8c-112">*configid*</span><span class="sxs-lookup"><span data-stu-id="36a8c-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="36a8c-113">Um valor que representa os dados de configuração a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="36a8c-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a8c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36a8c-114">Return value</span></span>

<span data-ttu-id="36a8c-115">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="36a8c-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="36a8c-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="36a8c-116">Return code</span></span>                                                                                                    | <span data-ttu-id="36a8c-117">Description</span><span class="sxs-lookup"><span data-stu-id="36a8c-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36a8c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36a8c-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="36a8c-119">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="36a8c-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="36a8c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="36a8c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="36a8c-121">*Configid* é 0 (um valor reservado para a configuração padrão).</span><span class="sxs-lookup"><span data-stu-id="36a8c-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="36a8c-122"><dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="36a8c-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="36a8c-123">Não foi possível encontrar *configid* .</span><span class="sxs-lookup"><span data-stu-id="36a8c-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="36a8c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a8c-124">Requirements</span></span>



| <span data-ttu-id="36a8c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a8c-125">Requirement</span></span> | <span data-ttu-id="36a8c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="36a8c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a8c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36a8c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="36a8c-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="36a8c-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="36a8c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36a8c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="36a8c-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="36a8c-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36a8c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36a8c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a8c-132"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="36a8c-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="36a8c-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="36a8c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36a8c-134"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36a8c-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a8c-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="36a8c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a8c-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="36a8c-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





