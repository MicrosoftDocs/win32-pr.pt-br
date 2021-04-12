---
title: Método ReactivateServer da classe Win32_TSLicenseServer
description: Reativa o servidor de licença Área de Trabalho Remota usando um novo identificador que foi obtido pelo telefone ou pela Internet.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReactivateServer
- Método ReactivateServer Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ReactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455144"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6142f-106">Método ReactivateServer da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="6142f-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6142f-107">Reativa o servidor de licença Área de Trabalho Remota usando um novo identificador que foi obtido pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="6142f-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="6142f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6142f-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6142f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6142f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6142f-110">*sNewLicenseServerId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6142f-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6142f-111">Área de Trabalho Remota ID do servidor de licença que foi obtida pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="6142f-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="6142f-112">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6142f-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6142f-113">O status de ativação retornado pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6142f-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="6142f-114">0</span><span class="sxs-lookup"><span data-stu-id="6142f-114">0</span></span>
</dt> <dd>

<span data-ttu-id="6142f-115">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="6142f-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="6142f-116">1</span><span class="sxs-lookup"><span data-stu-id="6142f-116">1</span></span>
</dt> <dd>

<span data-ttu-id="6142f-117">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="6142f-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="6142f-118">2</span><span class="sxs-lookup"><span data-stu-id="6142f-118">2</span></span>
</dt> <dd>

<span data-ttu-id="6142f-119">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6142f-119">An unknown error occurred.</span></span> <span data-ttu-id="6142f-120">Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="6142f-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6142f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6142f-121">Return value</span></span>

<span data-ttu-id="6142f-122">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6142f-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6142f-123">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6142f-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6142f-124">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6142f-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6142f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6142f-125">Remarks</span></span>

<span data-ttu-id="6142f-126">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="6142f-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6142f-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6142f-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6142f-128">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6142f-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6142f-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6142f-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6142f-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6142f-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6142f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6142f-131">Requirements</span></span>



| <span data-ttu-id="6142f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6142f-132">Requirement</span></span> | <span data-ttu-id="6142f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6142f-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6142f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6142f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6142f-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6142f-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6142f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6142f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6142f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6142f-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6142f-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="6142f-138">Namespace</span></span><br/>                | <span data-ttu-id="6142f-139">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6142f-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6142f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6142f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6142f-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6142f-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6142f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6142f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6142f-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6142f-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6142f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="6142f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6142f-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="6142f-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

