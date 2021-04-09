---
description: Valide um texto de configuração para exatidão sem defini-lo como ativo. Retorna 1 em caso de êxito, 0 em erro.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Método ValidateConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920138"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="a3e2c-104">Método ValidateConfiguration da classe Control</span><span class="sxs-lookup"><span data-stu-id="a3e2c-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="a3e2c-105">Valide um texto de configuração para exatidão sem defini-lo como ativo.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="a3e2c-106">Retorna 1 em caso de êxito, 0 em erro.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e2c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3e2c-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="a3e2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3e2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e2c-109">*Configuração* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-110">A configuração a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-111">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-112">Quando esse método retornar, se houver um erro, esse parâmetro conterá uma descrição do erro de validação para a operação.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-113">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-114">Quando esse método retorna, esse parâmetro contém uma descrição de quaisquer avisos de validação para a operação.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="a3e2c-115">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-116">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-117">Quando esse método retorna, esse parâmetro contém um conjunto de informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-118">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-119">Quando esse método retornar, se houver um erro de validação, esse parâmetro indicará o tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="a3e2c-120">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a3e2c-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="a3e2c-121">0</span><span class="sxs-lookup"><span data-stu-id="a3e2c-121">0</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-122">O argumento está ausente.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-123">1</span><span class="sxs-lookup"><span data-stu-id="a3e2c-123">1</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-124">O formato do argumento é inválido.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2c-125">2</span><span class="sxs-lookup"><span data-stu-id="a3e2c-125">2</span></span>
</dt> <dd>

<span data-ttu-id="a3e2c-126">Um argumento de configuração é inválido.</span><span class="sxs-lookup"><span data-stu-id="a3e2c-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e2c-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a3e2c-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a3e2c-128">0</span><span class="sxs-lookup"><span data-stu-id="a3e2c-128">0</span></span>

<span data-ttu-id="a3e2c-129">Falha</span><span class="sxs-lookup"><span data-stu-id="a3e2c-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3e2c-130">1</span><span class="sxs-lookup"><span data-stu-id="a3e2c-130">1</span></span>

<span data-ttu-id="a3e2c-131">Sucesso</span><span class="sxs-lookup"><span data-stu-id="a3e2c-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3e2c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3e2c-132">Requirements</span></span>



| <span data-ttu-id="a3e2c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e2c-133">Requirement</span></span> | <span data-ttu-id="a3e2c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e2c-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e2c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3e2c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e2c-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a3e2c-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a3e2c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3e2c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e2c-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a3e2c-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="a3e2c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3e2c-139">Namespace</span></span><br/>                | <span data-ttu-id="a3e2c-140">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="a3e2c-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="a3e2c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a3e2c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3e2c-142"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3e2c-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3e2c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e2c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e2c-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3e2c-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a3e2c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3e2c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e2c-146">**Control**</span><span class="sxs-lookup"><span data-stu-id="a3e2c-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




