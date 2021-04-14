---
title: Método Delete da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Exclui a política de autorização de recurso Área de Trabalho Remota atual (RD \ 160; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Delete
- Método Delete Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396a766fb307d1e8a912d614147a2bff2bd924c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369323"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="5af65-106">Método Delete da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="5af65-106">Delete method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="5af65-107">Exclui a RD RAP (política de autorização de recursos) Área de Trabalho Remota atual.</span><span class="sxs-lookup"><span data-stu-id="5af65-107">Deletes the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="5af65-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5af65-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="5af65-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5af65-109">Parameters</span></span>

<span data-ttu-id="5af65-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5af65-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5af65-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5af65-111">Return value</span></span>

<span data-ttu-id="5af65-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5af65-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5af65-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5af65-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5af65-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5af65-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5af65-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5af65-115">Remarks</span></span>

<span data-ttu-id="5af65-116">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="5af65-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5af65-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5af65-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5af65-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5af65-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5af65-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5af65-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5af65-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5af65-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5af65-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af65-121">Requirements</span></span>



| <span data-ttu-id="5af65-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af65-122">Requirement</span></span> | <span data-ttu-id="5af65-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5af65-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af65-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5af65-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5af65-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5af65-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5af65-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5af65-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5af65-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5af65-128">Namespace</span></span><br/>                | <span data-ttu-id="5af65-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5af65-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5af65-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5af65-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af65-131"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5af65-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af65-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5af65-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af65-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af65-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5af65-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5af65-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af65-135">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="5af65-135">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

