---
title: Método GetConfig INapComponentConfig (NapCommon. h)
description: Recupera a configuração do componente do validador da integridade do sistema (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Método GetConfig NAP
- Método GetConfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455722"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="da4d4-106">Método INapComponentConfig:: GetConfig</span><span class="sxs-lookup"><span data-stu-id="da4d4-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="da4d4-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="da4d4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="da4d4-108">O método **GetConfig** recupera a configuração do componente do validador da integridade do sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="da4d4-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4d4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da4d4-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="da4d4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da4d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4d4-111">*bCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="da4d4-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d4-112">O tamanho, em bytes, do blob de configuração de *dados* .</span><span class="sxs-lookup"><span data-stu-id="da4d4-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="da4d4-113">*dados* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="da4d4-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d4-114">Um ponteiro para o endereço dos dados de configuração do componente SHV.</span><span class="sxs-lookup"><span data-stu-id="da4d4-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="da4d4-115">Os dados de configuração exportados de um computador x86 usando o método **GetConfig** podem ser importados para um computador x64 usando o método [**setconfig**](inapcomponentconfig-setconfig.md) e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="da4d4-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="da4d4-116">Portanto, os dados de configuração devem estar em um formato independente de arquitetura, como XML.</span><span class="sxs-lookup"><span data-stu-id="da4d4-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="da4d4-117">Usar XML em vez de um fluxo de bytes torna mais fácil usar dados de configuração em diferentes arquiteturas.</span><span class="sxs-lookup"><span data-stu-id="da4d4-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="da4d4-118">Os elementos XML usados nos dados de configuração são determinados pelo implementador.</span><span class="sxs-lookup"><span data-stu-id="da4d4-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4d4-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da4d4-119">Return value</span></span>

<span data-ttu-id="da4d4-120">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="da4d4-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="da4d4-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="da4d4-121">Return code</span></span>                                                                                     | <span data-ttu-id="da4d4-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="da4d4-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="da4d4-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da4d4-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="da4d4-124">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="da4d4-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="da4d4-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="da4d4-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="da4d4-126">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="da4d4-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="da4d4-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="da4d4-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="da4d4-128">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="da4d4-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="da4d4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="da4d4-129">Remarks</span></span>

<span data-ttu-id="da4d4-130">O parâmetro de dados deve ser alocado pelo receptor (implementador de componente) usando **CoTaskMemAlloc** e liberado pelo chamador usando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="da4d4-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4d4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4d4-131">Requirements</span></span>



| <span data-ttu-id="da4d4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4d4-132">Requirement</span></span> | <span data-ttu-id="da4d4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="da4d4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4d4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da4d4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="da4d4-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="da4d4-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="da4d4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da4d4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="da4d4-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da4d4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da4d4-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da4d4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="da4d4-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="da4d4-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="da4d4-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="da4d4-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da4d4-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da4d4-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4d4-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="da4d4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4d4-143">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="da4d4-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="da4d4-144">**INapComponentConfig:: setconfig**</span><span class="sxs-lookup"><span data-stu-id="da4d4-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





