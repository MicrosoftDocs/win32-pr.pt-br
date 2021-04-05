---
title: Método ActivateServerAutomatic da classe Win32_TSLicenseServer
description: Ativa a Área de Trabalho Remota servidor de licença automaticamente pela Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ActivateServerAutomatic
- Método ActivateServerAutomatic Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ActivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918205"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="42894-106">Método ActivateServerAutomatic da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="42894-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="42894-107">Ativa a Área de Trabalho Remota servidor de licença automaticamente pela Internet.</span><span class="sxs-lookup"><span data-stu-id="42894-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="42894-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42894-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="42894-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42894-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42894-110">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="42894-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42894-111">O status de ativação retornado pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="42894-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="42894-112">0</span><span class="sxs-lookup"><span data-stu-id="42894-112">0</span></span>
</dt> <dd>

<span data-ttu-id="42894-113">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="42894-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="42894-114">1</span><span class="sxs-lookup"><span data-stu-id="42894-114">1</span></span>
</dt> <dd>

<span data-ttu-id="42894-115">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="42894-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="42894-116">2</span><span class="sxs-lookup"><span data-stu-id="42894-116">2</span></span>
</dt> <dd>

<span data-ttu-id="42894-117">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="42894-117">An unknown error occurred.</span></span> <span data-ttu-id="42894-118">Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="42894-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42894-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42894-119">Return value</span></span>

<span data-ttu-id="42894-120">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="42894-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="42894-121">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="42894-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="42894-122">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="42894-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="42894-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="42894-123">Remarks</span></span>

<span data-ttu-id="42894-124">Esse método falha, a menos que as propriedades **FirstName**, **LastName**, **Company** e **CountryRegion** sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="42894-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="42894-125">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="42894-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="42894-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="42894-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42894-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="42894-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42894-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="42894-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42894-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42894-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42894-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42894-130">Requirements</span></span>



| <span data-ttu-id="42894-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="42894-131">Requirement</span></span> | <span data-ttu-id="42894-132">Valor</span><span class="sxs-lookup"><span data-stu-id="42894-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="42894-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42894-133">Minimum supported client</span></span><br/> | <span data-ttu-id="42894-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42894-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="42894-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42894-135">Minimum supported server</span></span><br/> | <span data-ttu-id="42894-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42894-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="42894-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="42894-137">Namespace</span></span><br/>                | <span data-ttu-id="42894-138">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="42894-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="42894-139">MOF</span><span class="sxs-lookup"><span data-stu-id="42894-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42894-140"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42894-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="42894-141">DLL</span><span class="sxs-lookup"><span data-stu-id="42894-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42894-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42894-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42894-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="42894-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42894-144">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="42894-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

