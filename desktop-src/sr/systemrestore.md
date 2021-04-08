---
title: Classe SystemRestore
description: Fornece métodos para desabilitar e habilitar o monitoramento, listar pontos de restauração disponíveis e iniciar uma restauração no sistema local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Restauração do sistema de classe SystemRestore
- Restauração do sistema de classe SystemRestore, descrita
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009491"
---
# <a name="systemrestore-class"></a><span data-ttu-id="f3804-105">Classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="f3804-105">SystemRestore class</span></span>

<span data-ttu-id="f3804-106">Fornece métodos para desabilitar e habilitar o monitoramento, listar pontos de restauração disponíveis e iniciar uma restauração no sistema local.</span><span class="sxs-lookup"><span data-stu-id="f3804-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3804-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3804-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="f3804-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f3804-108">Members</span></span>

<span data-ttu-id="f3804-109">A classe **SystemRestore** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f3804-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="f3804-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3804-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3804-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3804-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3804-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3804-112">Methods</span></span>

<span data-ttu-id="f3804-113">A classe **SystemRestore** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f3804-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="f3804-114">Método</span><span class="sxs-lookup"><span data-stu-id="f3804-114">Method</span></span>                                                             | <span data-ttu-id="f3804-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3804-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="f3804-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="f3804-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="f3804-117">Cria um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="f3804-118">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="f3804-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="f3804-119">Desabilita o monitoramento em uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="f3804-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="f3804-120">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="f3804-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="f3804-121">Habilita o monitoramento em uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="f3804-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="f3804-122">**GetLastRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="f3804-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="f3804-123">Recupera o status da última restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="f3804-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="f3804-124">**Restaurar**</span><span class="sxs-lookup"><span data-stu-id="f3804-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="f3804-125">Inicia uma restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="f3804-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="f3804-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3804-126">Properties</span></span>

<span data-ttu-id="f3804-127">A classe **SystemRestore** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f3804-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3804-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="f3804-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3804-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f3804-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="f3804-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f3804-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3804-131">A hora em que a alteração de estado ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f3804-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f3804-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3804-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f3804-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="f3804-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f3804-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3804-135">A descrição a ser exibida para que o usuário possa identificar facilmente um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="f3804-136">O comprimento máximo de uma cadeia de caracteres ANSI é MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="f3804-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="f3804-137">O comprimento máximo de uma cadeia de caracteres Unicode é o máximo \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="f3804-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="f3804-138">Para obter mais informações, consulte [texto de descrição do ponto de restauração](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="f3804-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3804-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="f3804-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3804-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3804-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3804-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f3804-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3804-142">O tipo do evento.</span><span class="sxs-lookup"><span data-stu-id="f3804-142">The type of event.</span></span> <span data-ttu-id="f3804-143">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3804-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="f3804-144">Valor</span><span class="sxs-lookup"><span data-stu-id="f3804-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="f3804-145">Significado</span><span class="sxs-lookup"><span data-stu-id="f3804-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="f3804-146"><dt>**Iniciar \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="f3804-147">Uma alteração do sistema foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="f3804-147">A system change has begun.</span></span> <span data-ttu-id="f3804-148">Uma chamada aninhada subsequente não cria um novo ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="f3804-149">As chamadas subsequentes devem usar encerrar \_ alteração do sistema aninhada \_ \_ , não \_ alteração do sistema final \_ .</span><span class="sxs-lookup"><span data-stu-id="f3804-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="f3804-150"><dt>**Iniciar \_ \_Alteração do sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="f3804-151">Uma alteração do sistema foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="f3804-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="f3804-152"><dt>**Fim \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="f3804-153">Uma alteração do sistema foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="f3804-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="f3804-154"><dt>**Fim \_ \_Alteração do sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="f3804-155">Uma alteração do sistema foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="f3804-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f3804-156">**RestorePointType**</span><span class="sxs-lookup"><span data-stu-id="f3804-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3804-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3804-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3804-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f3804-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3804-159">O tipo de ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-159">The type of restore point.</span></span> <span data-ttu-id="f3804-160">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3804-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="f3804-161">Valor</span><span class="sxs-lookup"><span data-stu-id="f3804-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="f3804-162">Significado</span><span class="sxs-lookup"><span data-stu-id="f3804-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="f3804-163">Do <dt>**aplicativo \_ INSTALAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="f3804-164">Um aplicativo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f3804-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="f3804-165">Do <dt>**aplicativo \_ DESINSTALAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="f3804-166">Um aplicativo foi desinstalado.</span><span class="sxs-lookup"><span data-stu-id="f3804-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="f3804-167"><dt>**Cancelado \_ OPERAÇÃO**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="f3804-168">Um aplicativo precisa excluir o ponto de restauração criado.</span><span class="sxs-lookup"><span data-stu-id="f3804-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="f3804-169">Por exemplo, um aplicativo usaria esse sinalizador quando um usuário cancelar uma instalação.</span><span class="sxs-lookup"><span data-stu-id="f3804-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="f3804-170"><dt>**Dispositivo \_ do \_Instalação do driver**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="f3804-171">Um driver de dispositivo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f3804-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="f3804-172"><dt>**Modificar \_ CONFIGURAÇÕES**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="f3804-173">Um aplicativo teve recursos adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="f3804-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="f3804-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="f3804-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3804-175">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3804-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3804-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f3804-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3804-177">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="f3804-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f3804-178">O número de sequência do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3804-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3804-179">Remarks</span></span>

<span data-ttu-id="f3804-180">Você pode obter uma lista de pontos de restauração usando o método [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) para recuperar uma coleção de objetos **SystemRestore** .</span><span class="sxs-lookup"><span data-stu-id="f3804-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="f3804-181">Você pode usar as propriedades de classe para identificar o ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="f3804-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="f3804-182">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3804-182">Examples</span></span>

<span data-ttu-id="f3804-183">O script de exemplo a seguir enumera os pontos de restauração atuais.</span><span class="sxs-lookup"><span data-stu-id="f3804-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="f3804-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3804-184">Requirements</span></span>



| <span data-ttu-id="f3804-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3804-185">Requirement</span></span> | <span data-ttu-id="f3804-186">Valor</span><span class="sxs-lookup"><span data-stu-id="f3804-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f3804-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3804-187">Minimum supported client</span></span><br/> | <span data-ttu-id="f3804-188">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3804-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f3804-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3804-189">Minimum supported server</span></span><br/> | <span data-ttu-id="f3804-190">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f3804-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="f3804-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3804-191">Namespace</span></span><br/>                | <span data-ttu-id="f3804-192">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="f3804-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="f3804-193">MOF</span><span class="sxs-lookup"><span data-stu-id="f3804-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3804-194"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3804-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3804-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3804-196">Instrumentação de Gerenciamento do Windows</span><span class="sxs-lookup"><span data-stu-id="f3804-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

