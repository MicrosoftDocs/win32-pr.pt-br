---
title: Método SetSecurityLayer da classe Win32_TSGeneralSetting
description: O método SetSecurityLayer define a camada de segurança.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSecurityLayer
- Método SetSecurityLayer Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918548"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="1fba7-106">Método SetSecurityLayer da classe Win32 \_ TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="1fba7-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="1fba7-107">O método **SetSecurityLayer** define a camada de segurança.</span><span class="sxs-lookup"><span data-stu-id="1fba7-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fba7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fba7-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="1fba7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fba7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fba7-110">*SecurityLayer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fba7-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fba7-111">A camada de segurança a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1fba7-111">The security layer to set.</span></span> <span data-ttu-id="1fba7-112">Se o nível de criptografia atual for 1, um valor de 2 para *SecurityLayer* não será válido.</span><span class="sxs-lookup"><span data-stu-id="1fba7-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="1fba7-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (0)</span><span class="sxs-lookup"><span data-stu-id="1fba7-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1fba7-114">A comunicação entre o servidor e o cliente usará a criptografia RDP nativa.</span><span class="sxs-lookup"><span data-stu-id="1fba7-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="1fba7-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (1)</span><span class="sxs-lookup"><span data-stu-id="1fba7-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1fba7-116">A camada mais segura com suporte do cliente será usada.</span><span class="sxs-lookup"><span data-stu-id="1fba7-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="1fba7-117">Se houver suporte, o SSL (TLS 1,0) será usado.</span><span class="sxs-lookup"><span data-stu-id="1fba7-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="1fba7-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="1fba7-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fba7-119">O SSL (TLS 1,0) será usado para autenticação de servidor, bem como para criptografar todos os dados transferidos entre o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="1fba7-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="1fba7-120">Essa configuração requer que o servidor tenha um certificado compatível com SSL.</span><span class="sxs-lookup"><span data-stu-id="1fba7-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="1fba7-121">Essa configuração não é compatível com um valor de **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="1fba7-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fba7-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fba7-122">Return value</span></span>

<span data-ttu-id="1fba7-123">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="1fba7-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1fba7-124">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="1fba7-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fba7-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fba7-125">Remarks</span></span>

<span data-ttu-id="1fba7-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1fba7-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1fba7-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1fba7-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1fba7-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="1fba7-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1fba7-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1fba7-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fba7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fba7-130">Requirements</span></span>



| <span data-ttu-id="1fba7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fba7-131">Requirement</span></span> | <span data-ttu-id="1fba7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1fba7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fba7-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fba7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1fba7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fba7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fba7-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fba7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1fba7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fba7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fba7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fba7-137">Namespace</span></span><br/>                | <span data-ttu-id="1fba7-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="1fba7-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1fba7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1fba7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fba7-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fba7-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fba7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1fba7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fba7-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fba7-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fba7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fba7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fba7-144">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1fba7-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="1fba7-145">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="1fba7-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

