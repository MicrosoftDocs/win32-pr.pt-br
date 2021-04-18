---
description: Recupera o identificador de segurança e os sinalizadores usados para proteger uma chave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Método GetKeyProtectorAdSidInformation da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105800068"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="36da1-103">Método GetKeyProtectorAdSidInformation da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="36da1-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="36da1-104">O método **GetKeyProtectorAdSidInformation** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera o identificador de segurança e os sinalizadores usados para proteger uma chave.</span><span class="sxs-lookup"><span data-stu-id="36da1-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="36da1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36da1-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="36da1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36da1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36da1-107">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36da1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36da1-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="36da1-108">Type: **string**</span></span>

<span data-ttu-id="36da1-109">Um identificador de cadeia de caracteres que pode ser usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="36da1-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="36da1-110">*SidString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="36da1-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36da1-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="36da1-111">Type: **string**</span></span>

<span data-ttu-id="36da1-112">Uma cadeia de caracteres que contém o SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="36da1-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="36da1-113">*Sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="36da1-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36da1-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36da1-114">Type: **uint32**</span></span>

<span data-ttu-id="36da1-115">Sinalizadores que alteram o comportamento da função.</span><span class="sxs-lookup"><span data-stu-id="36da1-115">Flags that change the function behavior.</span></span> <span data-ttu-id="36da1-116">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="36da1-116">This can be one of the following values.</span></span>



| <span data-ttu-id="36da1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="36da1-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="36da1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="36da1-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="36da1-119"><dt>**FVE \_ \_Sinalizador DPAPI \_ ng \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="36da1-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="36da1-120">Nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="36da1-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="36da1-121"><dt>**FVE \_ \_Desbloqueio \_ de sinalizador DPAPI ng \_ \_ como \_ \_ conta de serviço**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="36da1-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="36da1-122">Especifica que o protetor baseado em SID foi protegido a uma conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="36da1-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="36da1-123">Se esse sinalizador for especificado, o chamador deverá garantir que ele esteja sendo executado como a conta de serviço apropriada antes de chamar [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (descartando a representação temporariamente, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="36da1-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36da1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36da1-124">Return value</span></span>

<span data-ttu-id="36da1-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36da1-125">Type: **uint32**</span></span>

<span data-ttu-id="36da1-126">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="36da1-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="36da1-127">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="36da1-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="36da1-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="36da1-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="36da1-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="36da1-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="36da1-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="36da1-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36da1-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="36da1-131">Remarks</span></span>

<span data-ttu-id="36da1-132">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="36da1-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36da1-133">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="36da1-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="36da1-134">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="36da1-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36da1-135">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="36da1-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36da1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36da1-136">Requirements</span></span>



| <span data-ttu-id="36da1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="36da1-137">Requirement</span></span> | <span data-ttu-id="36da1-138">Valor</span><span class="sxs-lookup"><span data-stu-id="36da1-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36da1-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36da1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="36da1-140">Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]</span><span class="sxs-lookup"><span data-stu-id="36da1-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36da1-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36da1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="36da1-142">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="36da1-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36da1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="36da1-143">Namespace</span></span><br/>                | <span data-ttu-id="36da1-144">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="36da1-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="36da1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="36da1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36da1-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36da1-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36da1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="36da1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36da1-148">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="36da1-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
