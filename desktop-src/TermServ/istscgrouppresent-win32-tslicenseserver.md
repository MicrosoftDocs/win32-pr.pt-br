---
title: Método IsTSCGroupPresent da classe Win32_TSLicenseServer
description: O IsTSCGroupPresent não está mais disponível para uso a partir do Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsTSCGroupPresent
- Método IsTSCGroupPresent Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009145"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c61d0-106">Método IsTSCGroupPresent da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="c61d0-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c61d0-107">\[O **IsTSCGroupPresent** não está mais disponível para uso a partir do Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="c61d0-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="c61d0-108">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c61d0-108">This method is not supported.</span></span>

<span data-ttu-id="c61d0-109">**Windows server 2008 R2 e Windows server 2008:** Recupera se o grupo local computadores Terminal Server existe no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="c61d0-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61d0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c61d0-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="c61d0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c61d0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61d0-112">*Presente* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c61d0-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c61d0-113">Valor booliano que indica se o grupo local de computadores Terminal Server existe.</span><span class="sxs-lookup"><span data-stu-id="c61d0-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61d0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c61d0-114">Return value</span></span>

<span data-ttu-id="c61d0-115">Retorna o **WBEM \_ E \_ não \_ tem suporte**.</span><span class="sxs-lookup"><span data-stu-id="c61d0-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="c61d0-116">**Windows server 2008 R2 e Windows server 2008:** Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c61d0-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c61d0-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c61d0-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c61d0-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c61d0-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c61d0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c61d0-119">Remarks</span></span>

<span data-ttu-id="c61d0-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="c61d0-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c61d0-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c61d0-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c61d0-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c61d0-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c61d0-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c61d0-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c61d0-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c61d0-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c61d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c61d0-125">Requirements</span></span>



| <span data-ttu-id="c61d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61d0-126">Requirement</span></span> | <span data-ttu-id="c61d0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c61d0-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61d0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c61d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c61d0-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c61d0-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c61d0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c61d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c61d0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c61d0-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c61d0-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c61d0-132">End of client support</span></span><br/>    | <span data-ttu-id="c61d0-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c61d0-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c61d0-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c61d0-134">End of server support</span></span><br/>    | <span data-ttu-id="c61d0-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c61d0-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="c61d0-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c61d0-136">Namespace</span></span><br/>                | <span data-ttu-id="c61d0-137">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c61d0-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c61d0-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c61d0-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c61d0-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c61d0-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c61d0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c61d0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c61d0-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c61d0-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61d0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c61d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61d0-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c61d0-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

