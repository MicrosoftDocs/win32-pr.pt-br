---
title: Método GetLicenseServerId da classe Win32_TSLicenseServer
description: Recupera o identificador do servidor de licença Área de Trabalho Remota se o servidor estiver ativado no momento.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetLicenseServerId
- Método GetLicenseServerId Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método GetLicenseServerId
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369451"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="e4387-106">Método GetLicenseServerId da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="e4387-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="e4387-107">Recupera o identificador do servidor de licença Área de Trabalho Remota se o servidor estiver ativado no momento.</span><span class="sxs-lookup"><span data-stu-id="e4387-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4387-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4387-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="e4387-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4387-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4387-110">*sLicenseServerId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4387-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4387-111">Área de Trabalho Remota identificador do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="e4387-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4387-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4387-112">Return value</span></span>

<span data-ttu-id="e4387-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e4387-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e4387-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e4387-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e4387-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4387-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4387-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4387-116">Remarks</span></span>

<span data-ttu-id="e4387-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e4387-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e4387-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e4387-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4387-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4387-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e4387-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e4387-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4387-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e4387-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4387-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4387-122">Requirements</span></span>



| <span data-ttu-id="e4387-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4387-123">Requirement</span></span> | <span data-ttu-id="e4387-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e4387-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4387-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4387-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4387-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e4387-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e4387-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4387-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4387-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4387-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e4387-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4387-129">Namespace</span></span><br/>                | <span data-ttu-id="e4387-130">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e4387-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e4387-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e4387-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4387-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4387-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4387-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4387-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4387-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4387-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4387-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4387-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4387-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="e4387-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

