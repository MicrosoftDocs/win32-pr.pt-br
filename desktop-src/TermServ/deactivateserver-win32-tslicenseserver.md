---
title: Método DeactivateServer da classe Win32_TSLicenseServer
description: Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeactivateServer
- Método DeactivateServer Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método DeactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918080"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a4175-106">Método DeactivateServer da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="a4175-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a4175-107">Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="a4175-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4175-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4175-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a4175-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4175-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4175-110">*sConfirmCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4175-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4175-111">Código de confirmação.</span><span class="sxs-lookup"><span data-stu-id="a4175-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="a4175-112">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4175-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4175-113">O status de ativação retornado pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="a4175-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="a4175-114">0</span><span class="sxs-lookup"><span data-stu-id="a4175-114">0</span></span>
</dt> <dd>

<span data-ttu-id="a4175-115">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="a4175-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="a4175-116">1</span><span class="sxs-lookup"><span data-stu-id="a4175-116">1</span></span>
</dt> <dd>

<span data-ttu-id="a4175-117">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="a4175-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="a4175-118">2</span><span class="sxs-lookup"><span data-stu-id="a4175-118">2</span></span>
</dt> <dd>

<span data-ttu-id="a4175-119">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a4175-119">An unknown error occurred.</span></span> <span data-ttu-id="a4175-120">Não é conhecido se o servidor de licença Serviços de Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="a4175-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4175-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4175-121">Return value</span></span>

<span data-ttu-id="a4175-122">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a4175-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a4175-123">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a4175-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a4175-124">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4175-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4175-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4175-125">Remarks</span></span>

<span data-ttu-id="a4175-126">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a4175-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a4175-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4175-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4175-128">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4175-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4175-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a4175-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4175-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4175-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4175-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4175-131">Requirements</span></span>



| <span data-ttu-id="a4175-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4175-132">Requirement</span></span> | <span data-ttu-id="a4175-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a4175-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4175-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4175-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a4175-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a4175-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a4175-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4175-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a4175-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4175-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a4175-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4175-138">Namespace</span></span><br/>                | <span data-ttu-id="a4175-139">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a4175-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a4175-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a4175-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4175-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4175-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4175-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a4175-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4175-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4175-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4175-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4175-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4175-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a4175-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

