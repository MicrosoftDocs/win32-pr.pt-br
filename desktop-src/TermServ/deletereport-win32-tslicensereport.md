---
title: Método DeleteReport da classe Win32_TSLicenseReport
description: Exclui um objeto de relatório no servidor de licença Área de Trabalho Remota. Esse não é um método estático.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteReport
- Método DeleteReport Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método DeleteReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499265"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="e114e-107">Método DeleteReport da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="e114e-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="e114e-108">Exclui um objeto de relatório no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="e114e-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="e114e-109">Esse não é um método estático.</span><span class="sxs-lookup"><span data-stu-id="e114e-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e114e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e114e-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="e114e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e114e-111">Parameters</span></span>

<span data-ttu-id="e114e-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e114e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e114e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e114e-113">Return value</span></span>

<span data-ttu-id="e114e-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e114e-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e114e-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e114e-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e114e-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e114e-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e114e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e114e-117">Remarks</span></span>

<span data-ttu-id="e114e-118">Esse não é um método estático.</span><span class="sxs-lookup"><span data-stu-id="e114e-118">This is not a static method.</span></span> <span data-ttu-id="e114e-119">Esse método deve ser chamado de um objeto de relatório de uso de licença por usuário.</span><span class="sxs-lookup"><span data-stu-id="e114e-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="e114e-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e114e-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e114e-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e114e-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e114e-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e114e-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e114e-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e114e-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e114e-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e114e-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e114e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e114e-125">Requirements</span></span>



| <span data-ttu-id="e114e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e114e-126">Requirement</span></span> | <span data-ttu-id="e114e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e114e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e114e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e114e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e114e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e114e-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e114e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e114e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e114e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e114e-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e114e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e114e-132">Namespace</span></span><br/>                | <span data-ttu-id="e114e-133">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e114e-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e114e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e114e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e114e-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e114e-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e114e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e114e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e114e-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e114e-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e114e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e114e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e114e-139">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="e114e-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

