---
title: Método InstallLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallLicenseKeyPack
- Método InstallLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método InstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918132"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="04765-106">Método InstallLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="04765-106">InstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="04765-107">Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="04765-107">Installs a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="04765-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04765-108">Syntax</span></span>


```mof
uint32 InstallLicenseKeyPack(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="04765-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04765-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04765-110">*sLicenseKeyPackId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04765-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04765-111">Contém o código de licença de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="04765-111">Contains the 35-character license code.</span></span> <span data-ttu-id="04765-112">Somente a cadeia de caracteres alfanumérica de 35 caracteres deve ser fornecida como entrada.</span><span class="sxs-lookup"><span data-stu-id="04765-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="04765-113">Nenhum hífen deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="04765-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="04765-114">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04765-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04765-115">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="04765-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04765-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04765-116">Return value</span></span>

<span data-ttu-id="04765-117">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="04765-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="04765-118">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="04765-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="04765-119">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="04765-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04765-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="04765-120">Remarks</span></span>

<span data-ttu-id="04765-121">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="04765-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="04765-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="04765-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="04765-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="04765-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04765-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="04765-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="04765-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="04765-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="04765-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04765-126">Requirements</span></span>



| <span data-ttu-id="04765-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04765-127">Requirement</span></span> | <span data-ttu-id="04765-128">Valor</span><span class="sxs-lookup"><span data-stu-id="04765-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="04765-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04765-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04765-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04765-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="04765-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04765-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04765-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04765-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="04765-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="04765-133">Namespace</span></span><br/>                | <span data-ttu-id="04765-134">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="04765-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="04765-135">MOF</span><span class="sxs-lookup"><span data-stu-id="04765-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04765-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04765-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="04765-137">DLL</span><span class="sxs-lookup"><span data-stu-id="04765-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04765-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04765-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04765-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="04765-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04765-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="04765-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

