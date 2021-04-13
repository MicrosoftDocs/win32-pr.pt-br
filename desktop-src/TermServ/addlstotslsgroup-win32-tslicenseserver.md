---
title: Método AddLStoTSLSGroup da classe Win32_TSLicenseServer
description: Adiciona o Área de Trabalho Remota servidor de licença ao grupo de servidores de licença do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) em um controlador de domínio no mesmo domínio que o servidor de licença do Área de Trabalho Remota.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddLStoTSLSGroup
- Método AddLStoTSLSGroup Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369456"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="8cd51-106">Método AddLStoTSLSGroup da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="8cd51-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="8cd51-107">Adiciona o Área de Trabalho Remota servidor de licença ao grupo de servidores de licença do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) em um controlador de domínio no mesmo domínio que o servidor de licença do Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8cd51-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd51-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cd51-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="8cd51-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cd51-109">Parameters</span></span>

<span data-ttu-id="8cd51-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8cd51-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cd51-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cd51-111">Return value</span></span>

<span data-ttu-id="8cd51-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8cd51-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8cd51-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8cd51-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8cd51-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8cd51-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cd51-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cd51-115">Remarks</span></span>

<span data-ttu-id="8cd51-116">Você deve ser um membro do grupo Admins. do domínio para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="8cd51-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="8cd51-117">O servidor de licença deve ser membro do grupo Área de Trabalho Remota servidores de licença se o servidor estiver configurado para usar o escopo de descoberta de domínio ou floresta.</span><span class="sxs-lookup"><span data-stu-id="8cd51-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="8cd51-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8cd51-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8cd51-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8cd51-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8cd51-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8cd51-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8cd51-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8cd51-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd51-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cd51-122">Requirements</span></span>



| <span data-ttu-id="8cd51-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd51-123">Requirement</span></span> | <span data-ttu-id="8cd51-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8cd51-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd51-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd51-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8cd51-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8cd51-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd51-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cd51-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8cd51-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cd51-129">Namespace</span></span><br/>                | <span data-ttu-id="8cd51-130">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8cd51-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8cd51-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8cd51-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cd51-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cd51-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cd51-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd51-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd51-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cd51-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cd51-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cd51-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd51-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="8cd51-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="8cd51-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="8cd51-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

