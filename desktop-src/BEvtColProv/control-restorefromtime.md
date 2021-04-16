---
description: Restaure a configuração ativa do coletor de um arquivo de backup, selecionado por um carimbo de data/hora.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Método RestoreFromTime da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747710"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="5c3fd-103">Método RestoreFromTime da classe Control</span><span class="sxs-lookup"><span data-stu-id="5c3fd-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="5c3fd-104">Restaure a configuração ativa do coletor de um arquivo de backup, selecionado por um carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c3fd-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="5c3fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c3fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c3fd-107">*TargetTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-108">Restaure para o arquivo de backup neste carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="5c3fd-109">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-110">*TargetTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-111">Restaure para o arquivo de backup neste carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="5c3fd-112">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-113">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-114">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="5c3fd-115">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="5c3fd-116">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-117">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-118">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="5c3fd-119">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="5c3fd-120">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-121">*NewTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-122">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="5c3fd-123">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-124">*NewTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-125">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="5c3fd-126">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-127">*OriginalTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-128">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="5c3fd-129">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-130">*OriginalTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-131">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="5c3fd-132">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5c3fd-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-133">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-134">A cadeia de texto com a explicação do erro.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-135">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-136">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-137">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-138">A cadeia de texto com informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-139">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-140">O tipo do erro: Observe que 0 ou ausente indica êxito.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="5c3fd-141">0</span><span class="sxs-lookup"><span data-stu-id="5c3fd-141">0</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-142">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="5c3fd-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-143">1</span><span class="sxs-lookup"><span data-stu-id="5c3fd-143">1</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-144">formato de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="5c3fd-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-145">2</span><span class="sxs-lookup"><span data-stu-id="5c3fd-145">2</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-146">valor de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="5c3fd-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-147">3</span><span class="sxs-lookup"><span data-stu-id="5c3fd-147">3</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-148">erro ao abrir o recurso (soquete)</span><span class="sxs-lookup"><span data-stu-id="5c3fd-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-149">4</span><span class="sxs-lookup"><span data-stu-id="5c3fd-149">4</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-150">erro de persistência (gravação de arquivo)</span><span class="sxs-lookup"><span data-stu-id="5c3fd-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="5c3fd-151">5</span><span class="sxs-lookup"><span data-stu-id="5c3fd-151">5</span></span>
</dt> <dd>

<span data-ttu-id="5c3fd-152">erro de atomicidade (o carimbo de data/hora antigo não corresponde)</span><span class="sxs-lookup"><span data-stu-id="5c3fd-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c3fd-153">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5c3fd-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5c3fd-154">0</span><span class="sxs-lookup"><span data-stu-id="5c3fd-154">0</span></span>

<span data-ttu-id="5c3fd-155">Falha</span><span class="sxs-lookup"><span data-stu-id="5c3fd-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5c3fd-156">1</span><span class="sxs-lookup"><span data-stu-id="5c3fd-156">1</span></span>

<span data-ttu-id="5c3fd-157">Sucesso</span><span class="sxs-lookup"><span data-stu-id="5c3fd-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c3fd-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c3fd-158">Requirements</span></span>



| <span data-ttu-id="5c3fd-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c3fd-159">Requirement</span></span> | <span data-ttu-id="5c3fd-160">Valor</span><span class="sxs-lookup"><span data-stu-id="5c3fd-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3fd-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3fd-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3fd-162">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5c3fd-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5c3fd-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3fd-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3fd-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5c3fd-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="5c3fd-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c3fd-165">Namespace</span></span><br/>                | <span data-ttu-id="5c3fd-166">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="5c3fd-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="5c3fd-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5c3fd-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c3fd-168"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c3fd-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c3fd-169">DLL</span><span class="sxs-lookup"><span data-stu-id="5c3fd-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c3fd-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c3fd-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5c3fd-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c3fd-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c3fd-172">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="5c3fd-172">**Control**</span></span>](control.md)
</dt> </dl>

 

