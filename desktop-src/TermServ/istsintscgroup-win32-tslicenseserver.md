---
title: Método IsTSinTSCGroup da classe Win32_TSLicenseServer
description: Recupera se um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) é membro do grupo local computadores Terminal Server no servidor de licença Área de Trabalho Remota.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsTSinTSCGroup
- Método IsTSinTSCGroup Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsTSinTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499725"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="04512-106">Método IsTSinTSCGroup da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="04512-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="04512-107">Recupera se um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) é membro do grupo local computadores Terminal Server no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="04512-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="04512-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04512-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="04512-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04512-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04512-110">*tsname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04512-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04512-111">Nome do servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="04512-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="04512-112">*IsMember* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04512-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04512-113">Valor booliano que indica se o servidor de Host da Sessão RD é membro do grupo local de computadores Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="04512-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04512-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04512-114">Return value</span></span>

<span data-ttu-id="04512-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="04512-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="04512-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="04512-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="04512-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="04512-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04512-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="04512-118">Remarks</span></span>

<span data-ttu-id="04512-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="04512-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="04512-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="04512-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="04512-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="04512-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04512-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="04512-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="04512-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="04512-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="04512-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04512-124">Requirements</span></span>



| <span data-ttu-id="04512-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="04512-125">Requirement</span></span> | <span data-ttu-id="04512-126">Valor</span><span class="sxs-lookup"><span data-stu-id="04512-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="04512-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04512-127">Minimum supported client</span></span><br/> | <span data-ttu-id="04512-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04512-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="04512-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04512-129">Minimum supported server</span></span><br/> | <span data-ttu-id="04512-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04512-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="04512-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="04512-131">Namespace</span></span><br/>                | <span data-ttu-id="04512-132">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="04512-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="04512-133">MOF</span><span class="sxs-lookup"><span data-stu-id="04512-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04512-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04512-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="04512-135">DLL</span><span class="sxs-lookup"><span data-stu-id="04512-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04512-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04512-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04512-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="04512-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04512-138">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="04512-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

