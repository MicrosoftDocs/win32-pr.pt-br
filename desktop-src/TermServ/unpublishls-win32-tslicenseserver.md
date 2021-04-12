---
title: Método UnpublishLS da classe Win32_TSLicenseServer
description: Cancelar a publicação de um servidor de licença Área de Trabalho Remota do Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UnpublishLS
- Método UnpublishLS Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método UnpublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ec183b5be8055dc30add5bc00a7eb537cd20f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499453"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="541f8-106">Método UnpublishLS da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="541f8-106">UnpublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="541f8-107">Cancelar a publicação de um servidor de licença Área de Trabalho Remota do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="541f8-107">Unpublishes a Remote Desktop license server from Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="541f8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="541f8-108">Syntax</span></span>


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a><span data-ttu-id="541f8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="541f8-109">Parameters</span></span>

<span data-ttu-id="541f8-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="541f8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="541f8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="541f8-111">Return value</span></span>

<span data-ttu-id="541f8-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="541f8-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="541f8-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="541f8-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="541f8-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="541f8-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="541f8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="541f8-115">Remarks</span></span>

<span data-ttu-id="541f8-116">Para chamar esse método, você deve estar conectado como um administrador corporativo à floresta na qual o servidor de licença é membro.</span><span class="sxs-lookup"><span data-stu-id="541f8-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="541f8-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="541f8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="541f8-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="541f8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="541f8-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="541f8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="541f8-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="541f8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="541f8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="541f8-121">Requirements</span></span>



| <span data-ttu-id="541f8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="541f8-122">Requirement</span></span> | <span data-ttu-id="541f8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="541f8-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="541f8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="541f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="541f8-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="541f8-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="541f8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="541f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="541f8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="541f8-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="541f8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="541f8-128">Namespace</span></span><br/>                | <span data-ttu-id="541f8-129">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="541f8-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="541f8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="541f8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="541f8-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="541f8-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="541f8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="541f8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="541f8-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="541f8-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="541f8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="541f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541f8-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="541f8-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

