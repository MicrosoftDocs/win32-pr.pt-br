---
description: Restaure a configuração ativa do coletor a partir do arquivo de backup anterior (determinado voltando do carimbo de data/hora original atual).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Método Undo da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750988"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="32310-103">Método Undo da classe Control</span><span class="sxs-lookup"><span data-stu-id="32310-103">Undo method of the Control class</span></span>

<span data-ttu-id="32310-104">Restaure a configuração ativa do coletor a partir do arquivo de backup anterior (determinado voltando do carimbo de data/hora original atual).</span><span class="sxs-lookup"><span data-stu-id="32310-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="32310-105">Se a configuração tiver sido definida apenas, isso significa desfazer essa alteração.</span><span class="sxs-lookup"><span data-stu-id="32310-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="32310-106">As chamadas consecutivas serão desfeitas para as configurações anteriores e anteriores.</span><span class="sxs-lookup"><span data-stu-id="32310-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="32310-107">Retorna 1 em caso de êxito, 0 em erro.</span><span class="sxs-lookup"><span data-stu-id="32310-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="32310-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32310-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="32310-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32310-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32310-110">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32310-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-111">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="32310-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="32310-112">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="32310-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="32310-113">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-114">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32310-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-115">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="32310-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="32310-116">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="32310-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="32310-117">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-118">*NewTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-119">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="32310-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="32310-120">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-121">*NewTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-122">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="32310-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="32310-123">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-124">*OriginalTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-125">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="32310-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="32310-126">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-127">*OriginalTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-128">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="32310-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="32310-129">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="32310-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="32310-130">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-131">A cadeia de texto com a explicação do erro.</span><span class="sxs-lookup"><span data-stu-id="32310-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="32310-132">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-133">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="32310-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="32310-134">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-135">A cadeia de texto com informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="32310-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="32310-136">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32310-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32310-137">O tipo do erro: Observe que 0 ou ausente indica êxito.</span><span class="sxs-lookup"><span data-stu-id="32310-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="32310-138">0</span><span class="sxs-lookup"><span data-stu-id="32310-138">0</span></span>
</dt> <dd>

<span data-ttu-id="32310-139">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="32310-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="32310-140">1</span><span class="sxs-lookup"><span data-stu-id="32310-140">1</span></span>
</dt> <dd>

<span data-ttu-id="32310-141">formato de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="32310-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="32310-142">2</span><span class="sxs-lookup"><span data-stu-id="32310-142">2</span></span>
</dt> <dd>

<span data-ttu-id="32310-143">valor de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="32310-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="32310-144">3</span><span class="sxs-lookup"><span data-stu-id="32310-144">3</span></span>
</dt> <dd>

<span data-ttu-id="32310-145">erro ao abrir o recurso (soquete)</span><span class="sxs-lookup"><span data-stu-id="32310-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="32310-146">4</span><span class="sxs-lookup"><span data-stu-id="32310-146">4</span></span>
</dt> <dd>

<span data-ttu-id="32310-147">erro de persistência (gravação de arquivo)</span><span class="sxs-lookup"><span data-stu-id="32310-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="32310-148">5</span><span class="sxs-lookup"><span data-stu-id="32310-148">5</span></span>
</dt> <dd>

<span data-ttu-id="32310-149">erro de atomicidade (o carimbo de data/hora antigo não corresponde)</span><span class="sxs-lookup"><span data-stu-id="32310-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32310-150">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="32310-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="32310-151">0</span><span class="sxs-lookup"><span data-stu-id="32310-151">0</span></span>

<span data-ttu-id="32310-152">Falha</span><span class="sxs-lookup"><span data-stu-id="32310-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="32310-153">1</span><span class="sxs-lookup"><span data-stu-id="32310-153">1</span></span>

<span data-ttu-id="32310-154">Sucesso</span><span class="sxs-lookup"><span data-stu-id="32310-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32310-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32310-155">Requirements</span></span>



| <span data-ttu-id="32310-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="32310-156">Requirement</span></span> | <span data-ttu-id="32310-157">Valor</span><span class="sxs-lookup"><span data-stu-id="32310-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32310-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32310-158">Minimum supported client</span></span><br/> | <span data-ttu-id="32310-159">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="32310-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="32310-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32310-160">Minimum supported server</span></span><br/> | <span data-ttu-id="32310-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="32310-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="32310-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="32310-162">Namespace</span></span><br/>                | <span data-ttu-id="32310-163">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="32310-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="32310-164">MOF</span><span class="sxs-lookup"><span data-stu-id="32310-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32310-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32310-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="32310-166">DLL</span><span class="sxs-lookup"><span data-stu-id="32310-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32310-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32310-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="32310-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="32310-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32310-169">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="32310-169">**Control**</span></span>](control.md)
</dt> </dl>

 

