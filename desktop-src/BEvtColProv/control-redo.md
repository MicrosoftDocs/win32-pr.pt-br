---
description: Redefina a configuração ativa do coletor a partir do arquivo de backup posterior (determinado ao avançar do carimbo de data/hora original atual). Se a configuração tiver sido desfeita, isso significará refazer a alteração desfeita.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Método redo da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088883"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="fdba7-104">Método redo da classe Control</span><span class="sxs-lookup"><span data-stu-id="fdba7-104">Redo method of the Control class</span></span>

<span data-ttu-id="fdba7-105">Redefina a configuração ativa do coletor a partir do arquivo de backup posterior (determinado ao avançar do carimbo de data/hora original atual).</span><span class="sxs-lookup"><span data-stu-id="fdba7-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="fdba7-106">Se a configuração tiver sido desfeita, isso significará refazer a alteração desfeita.</span><span class="sxs-lookup"><span data-stu-id="fdba7-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdba7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdba7-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="fdba7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdba7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdba7-109">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-110">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="fdba7-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="fdba7-111">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="fdba7-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="fdba7-112">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-113">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-114">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="fdba7-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="fdba7-115">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="fdba7-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="fdba7-116">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-117">*NewTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-118">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="fdba7-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="fdba7-119">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-120">*NewTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-121">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="fdba7-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="fdba7-122">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-123">*OriginalTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-124">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fdba7-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="fdba7-125">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-126">*OriginalTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-127">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fdba7-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="fdba7-128">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fdba7-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-129">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-130">A cadeia de texto com a explicação do erro.</span><span class="sxs-lookup"><span data-stu-id="fdba7-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-131">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-132">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="fdba7-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-133">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-134">A cadeia de texto com informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="fdba7-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-135">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-136">O tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="fdba7-136">The type of the error.</span></span> <span data-ttu-id="fdba7-137">Observe que 0 ou ausente indicam êxito.</span><span class="sxs-lookup"><span data-stu-id="fdba7-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="fdba7-138">0</span><span class="sxs-lookup"><span data-stu-id="fdba7-138">0</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-139">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="fdba7-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-140">1</span><span class="sxs-lookup"><span data-stu-id="fdba7-140">1</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-141">formato de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="fdba7-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-142">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-142">2</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-143">valor de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="fdba7-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-144">3</span><span class="sxs-lookup"><span data-stu-id="fdba7-144">3</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-145">erro ao abrir o recurso (soquete)</span><span class="sxs-lookup"><span data-stu-id="fdba7-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-146">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-146">4</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-147">erro de persistência (gravação de arquivo)</span><span class="sxs-lookup"><span data-stu-id="fdba7-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-148">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-148">5</span></span>
</dt> <dd>

<span data-ttu-id="fdba7-149">erro de atomicidade (o carimbo de data/hora antigo não corresponde)</span><span class="sxs-lookup"><span data-stu-id="fdba7-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdba7-150">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fdba7-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="fdba7-151">0</span><span class="sxs-lookup"><span data-stu-id="fdba7-151">0</span></span>

<span data-ttu-id="fdba7-152">Falha</span><span class="sxs-lookup"><span data-stu-id="fdba7-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fdba7-153">1</span><span class="sxs-lookup"><span data-stu-id="fdba7-153">1</span></span>

<span data-ttu-id="fdba7-154">Sucesso</span><span class="sxs-lookup"><span data-stu-id="fdba7-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdba7-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdba7-155">Requirements</span></span>



| <span data-ttu-id="fdba7-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdba7-156">Requirement</span></span> | <span data-ttu-id="fdba7-157">Valor</span><span class="sxs-lookup"><span data-stu-id="fdba7-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdba7-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdba7-158">Minimum supported client</span></span><br/> | <span data-ttu-id="fdba7-159">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fdba7-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdba7-160">Minimum supported server</span></span><br/> | <span data-ttu-id="fdba7-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fdba7-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="fdba7-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdba7-162">Namespace</span></span><br/>                | <span data-ttu-id="fdba7-163">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="fdba7-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="fdba7-164">MOF</span><span class="sxs-lookup"><span data-stu-id="fdba7-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdba7-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdba7-166">DLL</span><span class="sxs-lookup"><span data-stu-id="fdba7-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdba7-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fdba7-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdba7-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdba7-169">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="fdba7-169">**Control**</span></span>](control.md)
</dt> </dl>

 

