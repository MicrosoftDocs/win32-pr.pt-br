---
description: Se a configuração atual for um resultado da função desfazer/refazer/restaurar, o marcará como se ela estivesse definida explicitamente, de modo que o histórico preservará a hora em que foi definido e um arquivo de backup será criado para ele na próxima alteração de configuração.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Método Checkpoint da classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088886"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="153f4-103">Método Checkpoint da classe Control</span><span class="sxs-lookup"><span data-stu-id="153f4-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="153f4-104">Se a configuração atual for um resultado da função desfazer/refazer/restaurar, o marcará como se ela estivesse definida explicitamente, de modo que o histórico preservará a hora em que foi definido e um arquivo de backup será criado para ele na próxima alteração de configuração.</span><span class="sxs-lookup"><span data-stu-id="153f4-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="153f4-105">Se a configuração atual já foi definida explicitamente, não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="153f4-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="153f4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="153f4-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="153f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="153f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153f4-108">*OldTimestampLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="153f4-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-109">O carimbo de data/hora de quando a configuração atual foi definida.</span><span class="sxs-lookup"><span data-stu-id="153f4-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="153f4-110">Se não for 0, habilitará a verificação de atomicidade: a ação será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="153f4-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="153f4-111">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="153f4-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="153f4-112">*OldTimestampHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="153f4-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-113">O carimbo de data/hora de quando a configuração atual foi definida.</span><span class="sxs-lookup"><span data-stu-id="153f4-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="153f4-114">Se não for 0, habilitará a verificação de atomicidade: a ação será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas).</span><span class="sxs-lookup"><span data-stu-id="153f4-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="153f4-115">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="153f4-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="153f4-116">*Errostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="153f4-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-117">A cadeia de texto com a explicação do erro.</span><span class="sxs-lookup"><span data-stu-id="153f4-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-118">*Aviso de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="153f4-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-119">A cadeia de texto com avisos.</span><span class="sxs-lookup"><span data-stu-id="153f4-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-120">*Infostring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="153f4-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-121">A cadeia de texto com informações sobre a configuração.</span><span class="sxs-lookup"><span data-stu-id="153f4-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-122">*ErrorType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="153f4-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-123">O tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="153f4-123">The type of the error.</span></span> <span data-ttu-id="153f4-124">Observe que 0 ou ausente indicam êxito.</span><span class="sxs-lookup"><span data-stu-id="153f4-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="153f4-125">0</span><span class="sxs-lookup"><span data-stu-id="153f4-125">0</span></span>
</dt> <dd>

<span data-ttu-id="153f4-126">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="153f4-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-127">1</span><span class="sxs-lookup"><span data-stu-id="153f4-127">1</span></span>
</dt> <dd>

<span data-ttu-id="153f4-128">formato de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="153f4-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="153f4-129">2</span><span class="sxs-lookup"><span data-stu-id="153f4-129">2</span></span>
</dt> <dd>

<span data-ttu-id="153f4-130">valor de argumento inadequado</span><span class="sxs-lookup"><span data-stu-id="153f4-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="153f4-131">3</span><span class="sxs-lookup"><span data-stu-id="153f4-131">3</span></span>
</dt> <dd>

<span data-ttu-id="153f4-132">erro ao abrir o recurso (soquete)</span><span class="sxs-lookup"><span data-stu-id="153f4-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="153f4-133">4</span><span class="sxs-lookup"><span data-stu-id="153f4-133">4</span></span>
</dt> <dd>

<span data-ttu-id="153f4-134">erro de persistência (gravação de arquivo)</span><span class="sxs-lookup"><span data-stu-id="153f4-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="153f4-135">5</span><span class="sxs-lookup"><span data-stu-id="153f4-135">5</span></span>
</dt> <dd>

<span data-ttu-id="153f4-136">erro de atomicidade (o carimbo de data/hora antigo não corresponde)</span><span class="sxs-lookup"><span data-stu-id="153f4-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153f4-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="153f4-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="153f4-138">0</span><span class="sxs-lookup"><span data-stu-id="153f4-138">0</span></span>

<span data-ttu-id="153f4-139">Falha</span><span class="sxs-lookup"><span data-stu-id="153f4-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="153f4-140">1</span><span class="sxs-lookup"><span data-stu-id="153f4-140">1</span></span>

<span data-ttu-id="153f4-141">Sucesso</span><span class="sxs-lookup"><span data-stu-id="153f4-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="153f4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="153f4-142">Requirements</span></span>



| <span data-ttu-id="153f4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="153f4-143">Requirement</span></span> | <span data-ttu-id="153f4-144">Valor</span><span class="sxs-lookup"><span data-stu-id="153f4-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153f4-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="153f4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="153f4-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="153f4-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="153f4-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="153f4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="153f4-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="153f4-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="153f4-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="153f4-149">Namespace</span></span><br/>                | <span data-ttu-id="153f4-150">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="153f4-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="153f4-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="153f4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="153f4-152"><dt>Srrestoreptapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="153f4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="153f4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="153f4-154"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="153f4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="153f4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153f4-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="153f4-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="153f4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153f4-158">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="153f4-158">**Control**</span></span>](control.md)
</dt> </dl>

 

