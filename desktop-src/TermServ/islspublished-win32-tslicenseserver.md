---
title: Método IsLSPublished da classe Win32_TSLicenseServer
description: Recupera se o servidor de licença Área de Trabalho Remota está publicado no Active Directory Domain Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSPublished
- Método IsLSPublished Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764737"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f1490-106">Método IsLSPublished da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="f1490-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f1490-107">Recupera se o servidor de licença Área de Trabalho Remota está publicado no Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f1490-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1490-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1490-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="f1490-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1490-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1490-110">*Publicado* \[ em fora\]</span><span class="sxs-lookup"><span data-stu-id="f1490-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1490-111">Valor booliano que indica se o servidor de licença está publicado no AD DS.</span><span class="sxs-lookup"><span data-stu-id="f1490-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1490-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1490-112">Return value</span></span>

<span data-ttu-id="f1490-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="f1490-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f1490-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f1490-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f1490-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f1490-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1490-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1490-116">Remarks</span></span>

<span data-ttu-id="f1490-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="f1490-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f1490-118">Se o servidor de licença for publicado no AD DS, ele será detectável automaticamente pelos servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na mesma floresta.</span><span class="sxs-lookup"><span data-stu-id="f1490-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="f1490-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f1490-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f1490-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f1490-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f1490-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f1490-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f1490-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f1490-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1490-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1490-123">Requirements</span></span>



| <span data-ttu-id="f1490-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1490-124">Requirement</span></span> | <span data-ttu-id="f1490-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f1490-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1490-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1490-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1490-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1490-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f1490-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1490-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1490-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1490-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f1490-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1490-130">Namespace</span></span><br/>                | <span data-ttu-id="f1490-131">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f1490-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f1490-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f1490-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1490-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1490-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1490-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f1490-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1490-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1490-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1490-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1490-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1490-137">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f1490-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

