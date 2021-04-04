---
description: Defina a nova configuração ativa do coletor.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Método SetConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646220"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="ba4fd-103">Método SetConfiguration da classe Control</span><span class="sxs-lookup"><span data-stu-id="ba4fd-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="ba4fd-104">Defina a nova configuração ativa do coletor.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba4fd-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="ba4fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba4fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4fd-107">*Configuração* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-108">A configuração a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-109">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-110">Os bits de ordem inferior de um carimbo de data/hora que indica quando a configuração ativa atual foi definida.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="ba4fd-111">A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-112">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-113">Os bits de ordem superior de um carimbo de data/hora que indica quando a configuração ativa atual foi definida.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="ba4fd-114">A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-115">*NewTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-116">Quando esse método retorna, esse parâmetro contém os bits de ordem inferior de um carimbo de data/hora que indica quando a nova configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="ba4fd-117">A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-118">*NewTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-119">Quando esse método retorna, esse parâmetro contém os bits de ordem superior do carimbo de data/hora que indica quando a nova configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="ba4fd-120">A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-121">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-122">Quando esse método retornar, se houver um erro, esse parâmetro conterá a descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-123">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-124">Quando esse método retornar, esse parâmetro conterá quaisquer mensagens de avisos para a operação.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-125">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-126">Quando esse método retorna, esse parâmetro contém informações para a nova configuração ativa.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-127">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-128">Quando esse método retornar, se houver um erro, esse parâmetro indicará o tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="ba4fd-129">0</span><span class="sxs-lookup"><span data-stu-id="ba4fd-129">0</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-130">A nova configuração está ausente.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-131">1</span><span class="sxs-lookup"><span data-stu-id="ba4fd-131">1</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-132">O formato da nova configuração é inválido.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-133">2</span><span class="sxs-lookup"><span data-stu-id="ba4fd-133">2</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-134">A nova configuração é inválida.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-135">3</span><span class="sxs-lookup"><span data-stu-id="ba4fd-135">3</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-136">Ocorreu um erro causado por um Soquete aberto.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-137">4</span><span class="sxs-lookup"><span data-stu-id="ba4fd-137">4</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-138">Houve um erro de gravação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="ba4fd-139">5</span><span class="sxs-lookup"><span data-stu-id="ba4fd-139">5</span></span>
</dt> <dd>

<span data-ttu-id="ba4fd-140">Ocorreu um erro de atomicidade.</span><span class="sxs-lookup"><span data-stu-id="ba4fd-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4fd-141">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ba4fd-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ba4fd-142">0</span><span class="sxs-lookup"><span data-stu-id="ba4fd-142">0</span></span>

<span data-ttu-id="ba4fd-143">Falha</span><span class="sxs-lookup"><span data-stu-id="ba4fd-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ba4fd-144">1</span><span class="sxs-lookup"><span data-stu-id="ba4fd-144">1</span></span>

<span data-ttu-id="ba4fd-145">Sucesso</span><span class="sxs-lookup"><span data-stu-id="ba4fd-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba4fd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba4fd-146">Requirements</span></span>



| <span data-ttu-id="ba4fd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba4fd-147">Requirement</span></span> | <span data-ttu-id="ba4fd-148">Valor</span><span class="sxs-lookup"><span data-stu-id="ba4fd-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4fd-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba4fd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4fd-150">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ba4fd-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ba4fd-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba4fd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4fd-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba4fd-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="ba4fd-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba4fd-153">Namespace</span></span><br/>                | <span data-ttu-id="ba4fd-154">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="ba4fd-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="ba4fd-155">MOF</span><span class="sxs-lookup"><span data-stu-id="ba4fd-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba4fd-156"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba4fd-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba4fd-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ba4fd-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba4fd-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba4fd-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ba4fd-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba4fd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4fd-160">**Control**</span><span class="sxs-lookup"><span data-stu-id="ba4fd-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




