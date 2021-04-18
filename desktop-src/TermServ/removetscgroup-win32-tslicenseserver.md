---
title: Método RemoveTSCGroup da classe Win32_TSLicenseServer
description: O RemoveTSCGroup não está mais disponível para uso a partir do Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveTSCGroup
- Método RemoveTSCGroup Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499780"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="7865f-106">Método RemoveTSCGroup da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="7865f-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="7865f-107">\[O **RemoveTSCGroup** não está mais disponível para uso a partir do Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="7865f-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="7865f-108">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="7865f-108">This method is not supported.</span></span>

<span data-ttu-id="7865f-109">**Windows server 2008 R2 e Windows server 2008:** Remove o grupo local computadores Terminal Server do Área de Trabalho Remota servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="7865f-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7865f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7865f-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="7865f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7865f-111">Parameters</span></span>

<span data-ttu-id="7865f-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7865f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7865f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7865f-113">Return value</span></span>

<span data-ttu-id="7865f-114">Retorna o **WBEM \_ E \_ não \_ tem suporte**.</span><span class="sxs-lookup"><span data-stu-id="7865f-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="7865f-115">**Windows server 2008 R2 e Windows server 2008:** Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7865f-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7865f-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7865f-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7865f-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7865f-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7865f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7865f-118">Remarks</span></span>

<span data-ttu-id="7865f-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7865f-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7865f-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7865f-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7865f-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7865f-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7865f-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7865f-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7865f-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7865f-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7865f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7865f-124">Requirements</span></span>



| <span data-ttu-id="7865f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7865f-125">Requirement</span></span> | <span data-ttu-id="7865f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7865f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7865f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7865f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7865f-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7865f-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7865f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7865f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7865f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7865f-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7865f-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7865f-131">End of client support</span></span><br/>    | <span data-ttu-id="7865f-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7865f-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7865f-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7865f-133">End of server support</span></span><br/>    | <span data-ttu-id="7865f-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7865f-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="7865f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="7865f-135">Namespace</span></span><br/>                | <span data-ttu-id="7865f-136">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7865f-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7865f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="7865f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7865f-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7865f-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7865f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7865f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7865f-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7865f-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7865f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7865f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7865f-142">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="7865f-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="7865f-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="7865f-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

