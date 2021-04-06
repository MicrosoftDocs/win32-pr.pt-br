---
description: Restaure a configuração ativa do coletor de um arquivo de backup.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Método restorefile da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920140"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="2569b-103">Método restorefile da classe Control</span><span class="sxs-lookup"><span data-stu-id="2569b-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="2569b-104">Restaure a configuração ativa do coletor de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="2569b-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2569b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2569b-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="2569b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2569b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2569b-107">Do *arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2569b-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-108">Nome do arquivo de backup a ser restaurado da lista retornada por ListBackups ().</span><span class="sxs-lookup"><span data-stu-id="2569b-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="2569b-109">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2569b-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-110">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="2569b-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2569b-111">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="2569b-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2569b-112">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-113">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2569b-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-114">O carimbo de data/hora de quando a configuração anterior foi definida.</span><span class="sxs-lookup"><span data-stu-id="2569b-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2569b-115">Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="2569b-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2569b-116">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-117">*NewTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-118">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="2569b-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2569b-119">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-120">*NewTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-121">O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="2569b-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2569b-122">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-123">*OriginalTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-124">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="2569b-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2569b-125">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-126">*OriginalTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-127">O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="2569b-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2569b-128">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2569b-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2569b-129">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-130">A cadeia de texto com a explicação do erro.</span><span class="sxs-lookup"><span data-stu-id="2569b-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="2569b-131">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-132">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="2569b-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="2569b-133">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-134">A cadeia de texto com informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="2569b-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2569b-135">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2569b-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2569b-136">O tipo do erro: Observe que 0 ou ausente indica êxito.</span><span class="sxs-lookup"><span data-stu-id="2569b-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="2569b-137">0</span><span class="sxs-lookup"><span data-stu-id="2569b-137">0</span></span>
</dt> <dd>

<span data-ttu-id="2569b-138">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="2569b-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2569b-139">1</span><span class="sxs-lookup"><span data-stu-id="2569b-139">1</span></span>
</dt> <dd>

<span data-ttu-id="2569b-140">formato de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="2569b-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="2569b-141">2</span><span class="sxs-lookup"><span data-stu-id="2569b-141">2</span></span>
</dt> <dd>

<span data-ttu-id="2569b-142">valor de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="2569b-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="2569b-143">3</span><span class="sxs-lookup"><span data-stu-id="2569b-143">3</span></span>
</dt> <dd>

<span data-ttu-id="2569b-144">erro ao abrir o recurso (soquete)</span><span class="sxs-lookup"><span data-stu-id="2569b-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="2569b-145">4</span><span class="sxs-lookup"><span data-stu-id="2569b-145">4</span></span>
</dt> <dd>

<span data-ttu-id="2569b-146">erro de persistência (gravação de arquivo)</span><span class="sxs-lookup"><span data-stu-id="2569b-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="2569b-147">5</span><span class="sxs-lookup"><span data-stu-id="2569b-147">5</span></span>
</dt> <dd>

<span data-ttu-id="2569b-148">erro de atomicidade (o carimbo de data/hora antigo não corresponde)</span><span class="sxs-lookup"><span data-stu-id="2569b-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2569b-149">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2569b-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2569b-150">0</span><span class="sxs-lookup"><span data-stu-id="2569b-150">0</span></span>

<span data-ttu-id="2569b-151">Falha</span><span class="sxs-lookup"><span data-stu-id="2569b-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2569b-152">1</span><span class="sxs-lookup"><span data-stu-id="2569b-152">1</span></span>

<span data-ttu-id="2569b-153">Sucesso</span><span class="sxs-lookup"><span data-stu-id="2569b-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2569b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2569b-154">Requirements</span></span>



| <span data-ttu-id="2569b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2569b-155">Requirement</span></span> | <span data-ttu-id="2569b-156">Valor</span><span class="sxs-lookup"><span data-stu-id="2569b-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2569b-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2569b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2569b-158">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2569b-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2569b-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2569b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2569b-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2569b-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="2569b-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="2569b-161">Namespace</span></span><br/>                | <span data-ttu-id="2569b-162">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="2569b-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="2569b-163">MOF</span><span class="sxs-lookup"><span data-stu-id="2569b-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2569b-164"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2569b-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="2569b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2569b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2569b-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2569b-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2569b-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="2569b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2569b-168">**Control**</span><span class="sxs-lookup"><span data-stu-id="2569b-168">**Control**</span></span>](control.md)
</dt> </dl>

 

