---
title: Método INapComponentConfig3 SetConfigToID (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Método SetConfigToID NAP
- Método SetConfigToID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755583"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="0606c-106">Método INapComponentConfig3:: SetConfigToID</span><span class="sxs-lookup"><span data-stu-id="0606c-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="0606c-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0606c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0606c-108">O método **SetConfigToID** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="0606c-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0606c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0606c-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="0606c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0606c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0606c-111">*configid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0606c-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0606c-112">Um valor que representa a configuração.</span><span class="sxs-lookup"><span data-stu-id="0606c-112">A value that represents the configuration.</span></span> <span data-ttu-id="0606c-113">*Configid* é atribuído pelo serviço NPS (servidor de políticas de rede) e é exclusivo dentro do SHV.</span><span class="sxs-lookup"><span data-stu-id="0606c-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="0606c-114">Se *configid* for 0, a configuração padrão do SHV será definida.</span><span class="sxs-lookup"><span data-stu-id="0606c-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="0606c-115">*contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0606c-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0606c-116">O tamanho, em bytes, dos dados de configuração nos *dados*.</span><span class="sxs-lookup"><span data-stu-id="0606c-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="0606c-117">*dados* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0606c-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0606c-118">Na entrada, uma matriz de bytes que contém os dados de configuração definidos como *configid*.</span><span class="sxs-lookup"><span data-stu-id="0606c-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0606c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0606c-119">Return value</span></span>

<span data-ttu-id="0606c-120">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="0606c-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0606c-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0606c-121">Return code</span></span>                                                                                                    | <span data-ttu-id="0606c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="0606c-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0606c-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0606c-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="0606c-124">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="0606c-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="0606c-125"><dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="0606c-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="0606c-126">Não foi possível encontrar *configid* .</span><span class="sxs-lookup"><span data-stu-id="0606c-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="0606c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0606c-127">Remarks</span></span>

<span data-ttu-id="0606c-128">O método [**newconfig**](inapcomponentconfig3-newconfig.md) deve ser usado para alocar dados de configuração para *configid* antes que este método possa ser chamado.</span><span class="sxs-lookup"><span data-stu-id="0606c-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="0606c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0606c-129">Requirements</span></span>



| <span data-ttu-id="0606c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0606c-130">Requirement</span></span> | <span data-ttu-id="0606c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0606c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0606c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0606c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0606c-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0606c-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0606c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0606c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0606c-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0606c-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0606c-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0606c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0606c-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0606c-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0606c-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="0606c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0606c-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0606c-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0606c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0606c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0606c-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="0606c-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





