---
title: Método DeactivateServerAutomatic da classe Win32_TSLicenseServer
description: Desativa o servidor de licença Área de Trabalho Remota pela Internet.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeactivateServerAutomatic
- Método DeactivateServerAutomatic Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método DeactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009030"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a6d4e-106">Método DeactivateServerAutomatic da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="a6d4e-106">DeactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a6d4e-107">Desativa o servidor de licença Área de Trabalho Remota pela Internet.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-107">Deactivates the Remote Desktop license server over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d4e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6d4e-108">Syntax</span></span>


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a6d4e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6d4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6d4e-110">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a6d4e-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6d4e-111">O status de ativação retornado pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="a6d4e-112">0</span><span class="sxs-lookup"><span data-stu-id="a6d4e-112">0</span></span>
</dt> <dd>

<span data-ttu-id="a6d4e-113">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="a6d4e-114">1</span><span class="sxs-lookup"><span data-stu-id="a6d4e-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a6d4e-115">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="a6d4e-116">2</span><span class="sxs-lookup"><span data-stu-id="a6d4e-116">2</span></span>
</dt> <dd>

<span data-ttu-id="a6d4e-117">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-117">An unknown error occurred.</span></span> <span data-ttu-id="a6d4e-118">Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6d4e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6d4e-119">Return value</span></span>

<span data-ttu-id="a6d4e-120">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a6d4e-121">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a6d4e-122">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a6d4e-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d4e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6d4e-123">Remarks</span></span>

<span data-ttu-id="a6d4e-124">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a6d4e-125">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a6d4e-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6d4e-126">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a6d4e-127">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a6d4e-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6d4e-128">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a6d4e-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d4e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6d4e-129">Requirements</span></span>



| <span data-ttu-id="a6d4e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6d4e-130">Requirement</span></span> | <span data-ttu-id="a6d4e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a6d4e-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d4e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6d4e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d4e-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6d4e-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a6d4e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6d4e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d4e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6d4e-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a6d4e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6d4e-136">Namespace</span></span><br/>                | <span data-ttu-id="a6d4e-137">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a6d4e-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a6d4e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a6d4e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6d4e-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6d4e-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6d4e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a6d4e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6d4e-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6d4e-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d4e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6d4e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d4e-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d4e-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

