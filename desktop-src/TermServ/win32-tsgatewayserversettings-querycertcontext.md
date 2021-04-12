---
title: Método QueryCertContext da classe Win32_TSGatewayServerSettings
description: Indica se o certificado especificado está instalado.
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método QueryCertContext
- Método QueryCertContext Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método QueryCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455846"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="342c0-106">Método QueryCertContext da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="342c0-106">QueryCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="342c0-107">Indica se o certificado especificado está instalado.</span><span class="sxs-lookup"><span data-stu-id="342c0-107">Indicates whether the specified certificate is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="342c0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="342c0-108">Syntax</span></span>


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="342c0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="342c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="342c0-110">*CertHash* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="342c0-110">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="342c0-111">Hash do certificado usado pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="342c0-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="342c0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="342c0-112">Return value</span></span>

<span data-ttu-id="342c0-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="342c0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="342c0-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="342c0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="342c0-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="342c0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="342c0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="342c0-116">Remarks</span></span>

<span data-ttu-id="342c0-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="342c0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="342c0-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="342c0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="342c0-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="342c0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="342c0-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="342c0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="342c0-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="342c0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="342c0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="342c0-122">Requirements</span></span>



| <span data-ttu-id="342c0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="342c0-123">Requirement</span></span> | <span data-ttu-id="342c0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="342c0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="342c0-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="342c0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="342c0-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="342c0-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="342c0-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="342c0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="342c0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="342c0-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="342c0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="342c0-129">Namespace</span></span><br/>                | <span data-ttu-id="342c0-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="342c0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="342c0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="342c0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="342c0-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="342c0-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="342c0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="342c0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="342c0-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="342c0-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="342c0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="342c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342c0-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="342c0-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

