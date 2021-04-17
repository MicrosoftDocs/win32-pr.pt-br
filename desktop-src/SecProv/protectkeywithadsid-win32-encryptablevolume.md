---
description: Protege a chave de criptografia do volume usando um SID (identificador de segurança Active Directory).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Método ProtectKeyWithAdSid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784130"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="25329-103">Método ProtectKeyWithAdSid da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="25329-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="25329-104">O método **ProtectKeyWithAdSid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando um SID (identificador de segurança) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25329-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="25329-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25329-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="25329-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25329-107">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="25329-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25329-108">Uma cadeia de caracteres que especifica um identificador atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="25329-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="25329-109">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="25329-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="25329-110">*SidString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25329-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25329-111">Cadeia de caracteres que contém o Active Directory SID usado para proteger a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="25329-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="25329-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="25329-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25329-113">Sinalizadores que alteram o comportamento da função.</span><span class="sxs-lookup"><span data-stu-id="25329-113">Flags that change the function behavior.</span></span> <span data-ttu-id="25329-114">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="25329-114">This can be one of the following values.</span></span>



| <span data-ttu-id="25329-115">Valor</span><span class="sxs-lookup"><span data-stu-id="25329-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="25329-116">Significado</span><span class="sxs-lookup"><span data-stu-id="25329-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="25329-117"><dt>**FVE \_ \_Sinalizador DPAPI \_ ng \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="25329-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="25329-118">Nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="25329-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="25329-119"><dt>**FVE \_ \_Desbloqueio \_ de sinalizador DPAPI ng \_ \_ como \_ \_ conta de serviço**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="25329-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="25329-120">Especifica que o protetor baseado em SID foi protegido a uma conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="25329-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="25329-121">Se esse sinalizador for especificado, o chamador deverá garantir que ele esteja sendo executado como a conta de serviço apropriada antes de chamar [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (descartando a representação temporariamente, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="25329-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="25329-122">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="25329-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25329-123">Um identificador exclusivo associado ao protetor criado.</span><span class="sxs-lookup"><span data-stu-id="25329-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="25329-124">Você pode usar essa cadeia de caracteres para gerenciar o protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="25329-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="25329-125">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="25329-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25329-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25329-126">Return value</span></span>

<span data-ttu-id="25329-127">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="25329-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="25329-128">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="25329-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="25329-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="25329-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="25329-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="25329-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="25329-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="25329-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25329-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="25329-132">Remarks</span></span>

<span data-ttu-id="25329-133">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="25329-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25329-134">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="25329-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="25329-135">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="25329-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25329-136">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md)</span><span class="sxs-lookup"><span data-stu-id="25329-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="25329-137">Por padrão, você não pode adicionar uma conta de Active Directory ou um protetor de grupo remotamente.</span><span class="sxs-lookup"><span data-stu-id="25329-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="25329-138">Você deve habilitar a delegação restrita no controlador de domínio e no computador de origem.</span><span class="sxs-lookup"><span data-stu-id="25329-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="25329-139">No controlador de domínio, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="25329-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="25329-140">Abra o gerenciador de servidor.</span><span class="sxs-lookup"><span data-stu-id="25329-140">Open Server Manager</span></span>
2.  <span data-ttu-id="25329-141">Selecionar computadores em funções de Active Directory</span><span class="sxs-lookup"><span data-stu-id="25329-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="25329-142">Selecione o computador cliente de destino e clique com o botão direito do mouse</span><span class="sxs-lookup"><span data-stu-id="25329-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="25329-143">Selecione a guia Delegação</span><span class="sxs-lookup"><span data-stu-id="25329-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="25329-144">Selecione o botão de opção "confiar neste computador para delegação a serviços especificados"</span><span class="sxs-lookup"><span data-stu-id="25329-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="25329-145">Selecione o botão de opção "usar somente Kerberos"</span><span class="sxs-lookup"><span data-stu-id="25329-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="25329-146">Clique em Adicionar</span><span class="sxs-lookup"><span data-stu-id="25329-146">Click Add</span></span>
8.  <span data-ttu-id="25329-147">Selecione "usuários ou computadores"</span><span class="sxs-lookup"><span data-stu-id="25329-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="25329-148">Selecione host/como o nome da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="25329-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="25329-149">Execute as etapas 3 a 9 no computador de origem.</span><span class="sxs-lookup"><span data-stu-id="25329-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="25329-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25329-150">Requirements</span></span>



| <span data-ttu-id="25329-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="25329-151">Requirement</span></span> | <span data-ttu-id="25329-152">Valor</span><span class="sxs-lookup"><span data-stu-id="25329-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25329-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25329-153">Minimum supported client</span></span><br/> | <span data-ttu-id="25329-154">Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]</span><span class="sxs-lookup"><span data-stu-id="25329-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25329-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25329-155">Minimum supported server</span></span><br/> | <span data-ttu-id="25329-156">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="25329-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25329-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="25329-157">Namespace</span></span><br/>                | <span data-ttu-id="25329-158">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="25329-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="25329-159">MOF</span><span class="sxs-lookup"><span data-stu-id="25329-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25329-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25329-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25329-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="25329-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25329-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="25329-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
