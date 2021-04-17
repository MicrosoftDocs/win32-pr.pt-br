---
title: Classe SystemRestoreConfig
description: Fornece propriedades para controlar a frequência de criação de ponto de restauração agendada e a quantidade de espaço em disco consumida em cada unidade.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauração do sistema de classe SystemRestoreConfig
- Restauração do sistema de classe SystemRestoreConfig, descrita
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369709"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="73fd9-105">Classe SystemRestoreConfig</span><span class="sxs-lookup"><span data-stu-id="73fd9-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="73fd9-106">Fornece propriedades para controlar a frequência de criação de ponto de restauração agendada e a quantidade de espaço em disco consumida em cada unidade.</span><span class="sxs-lookup"><span data-stu-id="73fd9-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fd9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73fd9-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="73fd9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="73fd9-108">Members</span></span>

<span data-ttu-id="73fd9-109">A classe **SystemRestoreConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73fd9-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="73fd9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73fd9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73fd9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73fd9-111">Properties</span></span>

<span data-ttu-id="73fd9-112">A classe **SystemRestoreConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73fd9-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73fd9-113">**DiskPercent**</span><span class="sxs-lookup"><span data-stu-id="73fd9-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73fd9-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73fd9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73fd9-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73fd9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73fd9-116">A quantidade máxima de espaço em disco em cada unidade que pode ser usada pela restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="73fd9-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="73fd9-117">Esse valor é especificado como uma porcentagem do espaço total na unidade.</span><span class="sxs-lookup"><span data-stu-id="73fd9-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="73fd9-118">O valor padrão é 12%.</span><span class="sxs-lookup"><span data-stu-id="73fd9-118">The default value is 12 percent.</span></span>

<span data-ttu-id="73fd9-119">**Windows Vista:** Recebe um valor da Serviço de Cópias de Sombra de Volume (VSS).</span><span class="sxs-lookup"><span data-stu-id="73fd9-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="73fd9-120">Esta é a quantidade máxima de espaço em disco em cada unidade que pode ser usada pela restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="73fd9-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="73fd9-121">O valor padrão é 15% do espaço total da unidade ou 30 por cento do espaço livre disponível, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="73fd9-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="73fd9-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="73fd9-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73fd9-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73fd9-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73fd9-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73fd9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73fd9-125">O intervalo de tempo absoluto no qual os pontos de verificação do sistema agendados são criados, em segundos.</span><span class="sxs-lookup"><span data-stu-id="73fd9-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="73fd9-126">O valor padrão é 86.400 (24 horas).</span><span class="sxs-lookup"><span data-stu-id="73fd9-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="73fd9-127">**Windows Vista:** Recebe um valor do Agendador de tarefas para restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="73fd9-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="73fd9-128">Zero se a tarefa estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="73fd9-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="73fd9-129">**RPLifeInterval**</span><span class="sxs-lookup"><span data-stu-id="73fd9-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73fd9-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73fd9-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73fd9-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73fd9-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73fd9-132">O intervalo de tempo para o qual os pontos de restauração são preservados, em segundos.</span><span class="sxs-lookup"><span data-stu-id="73fd9-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="73fd9-133">Quando um ponto de restauração se torna mais antigo que esse intervalo especificado, ele é excluído.</span><span class="sxs-lookup"><span data-stu-id="73fd9-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="73fd9-134">O limite de idade padrão é de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="73fd9-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="73fd9-135">**Windows Vista:** Recebe um valor de **UINTMAX**.</span><span class="sxs-lookup"><span data-stu-id="73fd9-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="73fd9-136">**RPSessionInterval**</span><span class="sxs-lookup"><span data-stu-id="73fd9-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73fd9-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73fd9-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73fd9-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73fd9-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73fd9-139">O intervalo de tempo no qual os pontos de verificação do sistema agendados são criados durante a sessão, em segundos.</span><span class="sxs-lookup"><span data-stu-id="73fd9-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="73fd9-140">O valor padrão é zero, indicando que o recurso está desativado.</span><span class="sxs-lookup"><span data-stu-id="73fd9-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="73fd9-141">**Windows Vista:** Receberá zero se a restauração do sistema estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="73fd9-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="73fd9-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73fd9-142">Examples</span></span>

<span data-ttu-id="73fd9-143">Não há suporte para o código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="73fd9-143">The following sample code is not supported.</span></span> <span data-ttu-id="73fd9-144">Use a ferramenta de linha de comando Vssadmin.exe para alterar o tamanho do espaço reservado da unidade.</span><span class="sxs-lookup"><span data-stu-id="73fd9-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="73fd9-145">**Windows XP:** Há suporte para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="73fd9-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="73fd9-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73fd9-146">Requirements</span></span>



| <span data-ttu-id="73fd9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="73fd9-147">Requirement</span></span> | <span data-ttu-id="73fd9-148">Valor</span><span class="sxs-lookup"><span data-stu-id="73fd9-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73fd9-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73fd9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="73fd9-150">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="73fd9-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="73fd9-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73fd9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="73fd9-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="73fd9-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="73fd9-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="73fd9-153">Namespace</span></span><br/>                | <span data-ttu-id="73fd9-154">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="73fd9-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="73fd9-155">MOF</span><span class="sxs-lookup"><span data-stu-id="73fd9-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73fd9-156"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73fd9-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fd9-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="73fd9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fd9-158">Pontos de restauração</span><span class="sxs-lookup"><span data-stu-id="73fd9-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="73fd9-159">Instrumentação de Gerenciamento do Windows</span><span class="sxs-lookup"><span data-stu-id="73fd9-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

