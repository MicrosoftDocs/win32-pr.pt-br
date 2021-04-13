---
title: Método setconfig INapComponentConfig (NapCommon. h)
description: Define a configuração do componente do validador da integridade do sistema (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Método setconfig NAP
- Método setconfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método setconfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499857"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="254e2-106">Método INapComponentConfig:: setconfig</span><span class="sxs-lookup"><span data-stu-id="254e2-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="254e2-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="254e2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="254e2-108">O método **setconfig** define a configuração do componente do validador da integridade do sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="254e2-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="254e2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="254e2-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="254e2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="254e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="254e2-111">*bCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="254e2-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254e2-112">O tamanho, em bytes, do blob de configuração de *dados* .</span><span class="sxs-lookup"><span data-stu-id="254e2-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="254e2-113">*dados* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="254e2-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254e2-114">Um ponteiro para os dados de configuração do componente SHV.</span><span class="sxs-lookup"><span data-stu-id="254e2-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="254e2-115">Os dados de configuração exportados de um computador x86 usando o método [**GetConfig**](inapcomponentconfig-getconfig.md) podem ser importados para um computador x64 usando o método **setconfig** e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="254e2-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="254e2-116">Portanto, os dados de configuração devem estar em um formato independente de arquitetura, como XML.</span><span class="sxs-lookup"><span data-stu-id="254e2-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="254e2-117">Usar XML em vez de um fluxo de bytes torna mais fácil usar dados de configuração em diferentes arquiteturas.</span><span class="sxs-lookup"><span data-stu-id="254e2-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="254e2-118">Os elementos XML usados nos dados de configuração são determinados pelo implementador.</span><span class="sxs-lookup"><span data-stu-id="254e2-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="254e2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="254e2-119">Return value</span></span>

<span data-ttu-id="254e2-120">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="254e2-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="254e2-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="254e2-121">Return code</span></span>                                                                                     | <span data-ttu-id="254e2-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="254e2-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="254e2-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="254e2-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="254e2-124">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="254e2-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="254e2-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="254e2-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="254e2-126">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="254e2-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="254e2-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="254e2-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="254e2-128">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="254e2-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="254e2-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="254e2-129">Remarks</span></span>

<span data-ttu-id="254e2-130">As informações de controle de versão do componente devem ser incluídas no blob de configuração de *dados* .</span><span class="sxs-lookup"><span data-stu-id="254e2-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="254e2-131">As informações de controle de versão podem ser usadas ao migrar de uma versão de SHV para outra.</span><span class="sxs-lookup"><span data-stu-id="254e2-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="254e2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="254e2-132">Requirements</span></span>



| <span data-ttu-id="254e2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="254e2-133">Requirement</span></span> | <span data-ttu-id="254e2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="254e2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="254e2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="254e2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="254e2-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="254e2-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="254e2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="254e2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="254e2-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="254e2-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="254e2-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="254e2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="254e2-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="254e2-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="254e2-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="254e2-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="254e2-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="254e2-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="254e2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="254e2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="254e2-144">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="254e2-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="254e2-145">**INapConponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="254e2-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





