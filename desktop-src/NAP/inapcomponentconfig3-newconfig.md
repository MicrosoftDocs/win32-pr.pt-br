---
title: Método INapComponentConfig3 NewConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Método NewConfig NAP
- Método NewConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085372"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="7ae27-106">Método INapComponentConfig3:: NewConfig</span><span class="sxs-lookup"><span data-stu-id="7ae27-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="7ae27-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="7ae27-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7ae27-108">O método **newconfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="7ae27-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="7ae27-109">Quando essa função é chamada, um SHV deve alocar novos dados de configuração e preenchê-lo com uma cópia dos dados de configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="7ae27-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae27-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ae27-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="7ae27-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ae27-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae27-112">*configid*</span><span class="sxs-lookup"><span data-stu-id="7ae27-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="7ae27-113">Um valor que representa a configuração.</span><span class="sxs-lookup"><span data-stu-id="7ae27-113">A value that represents the configuration.</span></span> <span data-ttu-id="7ae27-114">*Configid* é atribuído pelo serviço NPS (servidor de políticas de rede) e é exclusivo dentro do SHV.</span><span class="sxs-lookup"><span data-stu-id="7ae27-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae27-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ae27-115">Return value</span></span>

<span data-ttu-id="7ae27-116">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="7ae27-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="7ae27-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7ae27-117">Return code</span></span>                                                                                                 | <span data-ttu-id="7ae27-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae27-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ae27-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ae27-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="7ae27-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="7ae27-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7ae27-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ae27-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="7ae27-122">*Configid* é 0 (um valor reservado para a configuração padrão).</span><span class="sxs-lookup"><span data-stu-id="7ae27-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="7ae27-123"><dt>**a \_ configuração de NAP E \_ SHV \_ \_ existia**</dt></span><span class="sxs-lookup"><span data-stu-id="7ae27-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="7ae27-124">*Configid* já existe.</span><span class="sxs-lookup"><span data-stu-id="7ae27-124">*ConfigID* already exists.</span></span> <span data-ttu-id="7ae27-125">A lista de IDs conhecida pelo NPS é diferente do SHV.</span><span class="sxs-lookup"><span data-stu-id="7ae27-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ae27-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ae27-126">Remarks</span></span>

<span data-ttu-id="7ae27-127">Depois que a nova configuração é criada por **newconfig**, os métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) devem ser usados para alterar a configuração conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7ae27-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae27-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ae27-128">Requirements</span></span>



| <span data-ttu-id="7ae27-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ae27-129">Requirement</span></span> | <span data-ttu-id="7ae27-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7ae27-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae27-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ae27-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae27-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7ae27-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7ae27-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ae27-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae27-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7ae27-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ae27-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ae27-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae27-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae27-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ae27-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="7ae27-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ae27-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ae27-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae27-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ae27-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae27-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="7ae27-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





