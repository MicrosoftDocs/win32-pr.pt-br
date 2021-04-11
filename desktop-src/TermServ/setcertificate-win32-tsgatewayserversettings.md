---
title: Método SetCertificate da classe Win32_TSGatewayServerSettings
description: Define o hash de certificado para associação HTTPS na porta 443 no IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetCertificate
- Método SetCertificate Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086278"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="da429-106">Método SetCertificate da \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="da429-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="da429-107">Define o hash de certificado para associação HTTPS na porta 443 no IIS.</span><span class="sxs-lookup"><span data-stu-id="da429-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="da429-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da429-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="da429-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da429-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da429-110">*CertHash* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da429-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da429-111">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="da429-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="da429-112">O novo hash de certificado.</span><span class="sxs-lookup"><span data-stu-id="da429-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da429-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da429-113">Return value</span></span>

<span data-ttu-id="da429-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da429-114">Type: **uint32**</span></span>

<span data-ttu-id="da429-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="da429-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="da429-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="da429-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="da429-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="da429-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da429-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="da429-118">Remarks</span></span>

<span data-ttu-id="da429-119">Depois que o hash de certificado tiver sido definido com esse método, você deverá chamar o método [**Configure**](configure-win32-tsgatewayserversettings.md) para concluir o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="da429-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="da429-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="da429-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="da429-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="da429-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da429-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="da429-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da429-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="da429-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da429-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da429-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da429-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da429-125">Requirements</span></span>



| <span data-ttu-id="da429-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="da429-126">Requirement</span></span> | <span data-ttu-id="da429-127">Valor</span><span class="sxs-lookup"><span data-stu-id="da429-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da429-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da429-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da429-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="da429-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="da429-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da429-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da429-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da429-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="da429-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="da429-132">Namespace</span></span><br/>                | <span data-ttu-id="da429-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="da429-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="da429-134">MOF</span><span class="sxs-lookup"><span data-stu-id="da429-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da429-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da429-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="da429-136">DLL</span><span class="sxs-lookup"><span data-stu-id="da429-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da429-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da429-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="da429-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="da429-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da429-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="da429-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

