---
title: Método ActivateServer da classe Win32_TSLicenseServer
description: Ativa o Área de Trabalho Remota servidor de licença usando um identificador de servidor de licença Área de Trabalho Remota que é obtido pelo telefone ou pela Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ActivateServer
- Método ActivateServer Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779282"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="abfd2-106">Método ActivateServer da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="abfd2-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="abfd2-107">Ativa o Área de Trabalho Remota servidor de licença usando um identificador de servidor de licença Área de Trabalho Remota que é obtido pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="abfd2-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfd2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abfd2-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="abfd2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abfd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfd2-110">*sLicenseServerId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abfd2-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfd2-111">Área de Trabalho Remota ID do servidor de licença que foi obtida pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="abfd2-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="abfd2-112">O parâmetro *sLicenseServerId* é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.</span><span class="sxs-lookup"><span data-stu-id="abfd2-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="abfd2-113">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abfd2-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abfd2-114">O status de ativação retornado pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="abfd2-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="abfd2-115">0</span><span class="sxs-lookup"><span data-stu-id="abfd2-115">0</span></span>
</dt> <dd>

<span data-ttu-id="abfd2-116">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="abfd2-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="abfd2-117">1</span><span class="sxs-lookup"><span data-stu-id="abfd2-117">1</span></span>
</dt> <dd>

<span data-ttu-id="abfd2-118">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="abfd2-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="abfd2-119">2</span><span class="sxs-lookup"><span data-stu-id="abfd2-119">2</span></span>
</dt> <dd>

<span data-ttu-id="abfd2-120">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="abfd2-120">An unknown error occurred.</span></span> <span data-ttu-id="abfd2-121">Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="abfd2-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfd2-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abfd2-122">Return value</span></span>

<span data-ttu-id="abfd2-123">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="abfd2-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="abfd2-124">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="abfd2-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="abfd2-125">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="abfd2-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abfd2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="abfd2-126">Remarks</span></span>

<span data-ttu-id="abfd2-127">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="abfd2-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="abfd2-128">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="abfd2-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="abfd2-129">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="abfd2-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="abfd2-130">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="abfd2-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="abfd2-131">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="abfd2-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="abfd2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abfd2-132">Requirements</span></span>



| <span data-ttu-id="abfd2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="abfd2-133">Requirement</span></span> | <span data-ttu-id="abfd2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="abfd2-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="abfd2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abfd2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="abfd2-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="abfd2-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="abfd2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abfd2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="abfd2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abfd2-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="abfd2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="abfd2-139">Namespace</span></span><br/>                | <span data-ttu-id="abfd2-140">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="abfd2-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="abfd2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="abfd2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abfd2-142"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abfd2-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="abfd2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="abfd2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abfd2-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abfd2-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfd2-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="abfd2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfd2-146">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="abfd2-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

