---
title: Método CreateRestorePoint da classe SystemRestore
description: Cria um ponto de restauração.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Restauração do sistema do método CreateRestorePoint
- CreateRestorePoint método de restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455289"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="85662-106">Método CreateRestorePoint da classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="85662-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="85662-107">Cria um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-107">Creates a restore point.</span></span>

<span data-ttu-id="85662-108">Esse método é o equivalente programável da função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .</span><span class="sxs-lookup"><span data-stu-id="85662-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="85662-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85662-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="85662-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85662-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85662-111">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="85662-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85662-112">A descrição a ser exibida para que o usuário possa identificar facilmente um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="85662-113">O comprimento máximo de uma cadeia de caracteres ANSI é MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="85662-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="85662-114">O comprimento máximo de uma cadeia de caracteres Unicode é o máximo \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="85662-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="85662-115">Para obter mais informações, consulte [texto de descrição do ponto de restauração](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="85662-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="85662-116">*RestorePointType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85662-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85662-117">O tipo de ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-117">The type of restore point.</span></span> <span data-ttu-id="85662-118">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="85662-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="85662-119">Tipo de ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="85662-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="85662-120">Significado</span><span class="sxs-lookup"><span data-stu-id="85662-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="85662-121">Do <dt>**aplicativo \_ INSTALAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="85662-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="85662-122">Um aplicativo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="85662-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="85662-123">Do <dt>**aplicativo \_ DESINSTALAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85662-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="85662-124">Um aplicativo foi desinstalado.</span><span class="sxs-lookup"><span data-stu-id="85662-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="85662-125"><dt>**Dispositivo \_ do \_Instalação do driver**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="85662-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="85662-126">Um driver de dispositivo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="85662-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="85662-127"><dt>**Modificar \_ CONFIGURAÇÕES**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="85662-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="85662-128">Um aplicativo teve recursos adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="85662-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="85662-129"><dt>**Cancelado \_ OPERAÇÃO**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="85662-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="85662-130">Um aplicativo precisa excluir o ponto de restauração criado.</span><span class="sxs-lookup"><span data-stu-id="85662-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="85662-131">Por exemplo, um aplicativo usaria esse sinalizador quando um usuário cancelar uma instalação.</span><span class="sxs-lookup"><span data-stu-id="85662-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85662-132">*EventType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85662-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85662-133">O tipo do evento.</span><span class="sxs-lookup"><span data-stu-id="85662-133">The type of event.</span></span> <span data-ttu-id="85662-134">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="85662-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="85662-135">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="85662-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="85662-136">Significado</span><span class="sxs-lookup"><span data-stu-id="85662-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="85662-137"><dt>**Iniciar \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="85662-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="85662-138">Uma alteração do sistema foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="85662-138">A system change has begun.</span></span> <span data-ttu-id="85662-139">Uma chamada aninhada subsequente não cria um novo ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="85662-140">As chamadas subsequentes devem usar encerrar \_ alteração do sistema aninhada \_ \_ , não \_ alteração do sistema final \_ .</span><span class="sxs-lookup"><span data-stu-id="85662-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="85662-141"><dt>**Iniciar \_ \_Alteração do sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="85662-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="85662-142">Uma alteração do sistema foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="85662-142">A system change has begun.</span></span> <br/> <span data-ttu-id="85662-143">Uma chamada subsequente deve usar A \_ alteração do sistema final \_ , e não encerrar a \_ alteração do sistema aninhado \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="85662-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="85662-144"><dt>**Fim \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="85662-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="85662-145">Uma alteração do sistema foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="85662-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="85662-146"><dt>**Fim \_ \_Alteração do sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="85662-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="85662-147">Uma alteração do sistema foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="85662-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85662-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85662-148">Return value</span></span>

<span data-ttu-id="85662-149">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85662-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85662-150">Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.</span><span class="sxs-lookup"><span data-stu-id="85662-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="85662-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="85662-151">Remarks</span></span>

<span data-ttu-id="85662-152">\* \* Windows 8: \* \*</span><span class="sxs-lookup"><span data-stu-id="85662-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="85662-153">Uma nova chave do Registro permite que os desenvolvedores de aplicativos alterem a frequência da criação do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="85662-154">Os aplicativos devem criar essa chave para usá-la porque ela não existirá no sistema.</span><span class="sxs-lookup"><span data-stu-id="85662-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="85662-155">O seguinte será aplicado por padrão se a chave não existir.</span><span class="sxs-lookup"><span data-stu-id="85662-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="85662-156">Se um aplicativo chamar o método **CreateRestorePoint** para criar um ponto de restauração, o Windows ignorará a criação desse novo ponto de restauração se quaisquer pontos de restauração tiverem sido criados nas últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="85662-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="85662-157">O método **CreateRestorePoint** retorna **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="85662-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="85662-158">Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **SystemRestorePointCreationFrequency** na chave do registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**.</span><span class="sxs-lookup"><span data-stu-id="85662-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="85662-159">O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="85662-160">O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="85662-161">Se o aplicativo chamar **CreateRestorePoint** para criar um ponto de restauração e o valor da chave do registro for 0, a restauração do sistema não ignorará a criação do novo ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="85662-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="85662-162">Se o aplicativo chamar **CreateRestorePoint** para criar um ponto de restauração e o valor da chave do registro for o inteiro N, a restauração do sistema ignorará a criação de um novo ponto de restauração se qualquer ponto de restauração tiver sido criado nos N minutos anteriores.</span><span class="sxs-lookup"><span data-stu-id="85662-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="85662-163">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85662-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="85662-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85662-164">Requirements</span></span>



| <span data-ttu-id="85662-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="85662-165">Requirement</span></span> | <span data-ttu-id="85662-166">Valor</span><span class="sxs-lookup"><span data-stu-id="85662-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="85662-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85662-167">Minimum supported client</span></span><br/> | <span data-ttu-id="85662-168">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="85662-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="85662-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85662-169">Minimum supported server</span></span><br/> | <span data-ttu-id="85662-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="85662-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="85662-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="85662-171">Namespace</span></span><br/>                | <span data-ttu-id="85662-172">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="85662-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="85662-173">MOF</span><span class="sxs-lookup"><span data-stu-id="85662-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85662-174"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85662-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85662-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="85662-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85662-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="85662-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





