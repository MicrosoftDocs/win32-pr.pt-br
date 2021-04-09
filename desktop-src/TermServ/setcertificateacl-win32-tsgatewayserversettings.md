---
title: Método SetCertificateACL da classe Win32_TSGatewayServerSettings
description: Define o certificado necessário para acessar o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetCertificateACL
- Método SetCertificateACL Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetCertificateACL
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7a43e737b39b9bea18ee3925b5c3f55440d2a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009731"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="396b4-106">Método SetCertificateACL da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="396b4-106">SetCertificateACL method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="396b4-107">Define o certificado necessário para acessar o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="396b4-107">Sets the certificate that is required to access the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="396b4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="396b4-108">Syntax</span></span>


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="396b4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="396b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396b4-110">*CertHash* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396b4-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396b4-111">Hash do certificado usado pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="396b4-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396b4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="396b4-112">Return value</span></span>

<span data-ttu-id="396b4-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="396b4-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="396b4-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="396b4-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="396b4-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="396b4-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="396b4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="396b4-116">Remarks</span></span>

<span data-ttu-id="396b4-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="396b4-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="396b4-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="396b4-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="396b4-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="396b4-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="396b4-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="396b4-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="396b4-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="396b4-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="396b4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="396b4-122">Requirements</span></span>



| <span data-ttu-id="396b4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="396b4-123">Requirement</span></span> | <span data-ttu-id="396b4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="396b4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="396b4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="396b4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="396b4-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="396b4-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="396b4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="396b4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="396b4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="396b4-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="396b4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="396b4-129">Namespace</span></span><br/>                | <span data-ttu-id="396b4-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="396b4-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="396b4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="396b4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="396b4-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="396b4-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="396b4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="396b4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="396b4-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="396b4-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="396b4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="396b4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396b4-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="396b4-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

