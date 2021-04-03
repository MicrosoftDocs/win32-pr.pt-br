---
title: Método INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Método GetConfigFromID NAP
- Método GetConfigFromID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644509"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="d4db1-106">Método INapComponentConfig3:: GetConfigFromID</span><span class="sxs-lookup"><span data-stu-id="d4db1-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="d4db1-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4db1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4db1-108">O método **GetConfigFromID** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="d4db1-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4db1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4db1-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="d4db1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4db1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4db1-111">*configid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4db1-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4db1-112">Um valor que representa a configuração.</span><span class="sxs-lookup"><span data-stu-id="d4db1-112">A value that represents the configuration.</span></span> <span data-ttu-id="d4db1-113">Se *configid* for **0**, o SHV deverá retornar os dados de configuração padrão em *OutData*.</span><span class="sxs-lookup"><span data-stu-id="d4db1-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="d4db1-114">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="d4db1-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4db1-115">O tamanho, em bytes, dos dados de configuração retornados em *OutData*.</span><span class="sxs-lookup"><span data-stu-id="d4db1-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="d4db1-116">*OutData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4db1-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4db1-117">No retorno, uma matriz de bytes que contém os dados de configuração representados por *configid*.</span><span class="sxs-lookup"><span data-stu-id="d4db1-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4db1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4db1-118">Return value</span></span>

<span data-ttu-id="d4db1-119">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="d4db1-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="d4db1-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4db1-120">Return code</span></span>                                                                                                    | <span data-ttu-id="d4db1-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4db1-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d4db1-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4db1-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="d4db1-123">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="d4db1-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="d4db1-124"><dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="d4db1-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d4db1-125">Não foi possível encontrar *configid* .</span><span class="sxs-lookup"><span data-stu-id="d4db1-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d4db1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4db1-126">Remarks</span></span>

<span data-ttu-id="d4db1-127">O método [**newconfig**](inapcomponentconfig3-newconfig.md) deve ser usado para alocar dados de configuração para *configid* antes que este método possa ser chamado.</span><span class="sxs-lookup"><span data-stu-id="d4db1-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4db1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4db1-128">Requirements</span></span>



| <span data-ttu-id="d4db1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4db1-129">Requirement</span></span> | <span data-ttu-id="d4db1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d4db1-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4db1-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4db1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d4db1-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4db1-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d4db1-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4db1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d4db1-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d4db1-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4db1-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4db1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4db1-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4db1-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4db1-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="d4db1-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4db1-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4db1-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4db1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4db1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4db1-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="d4db1-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





