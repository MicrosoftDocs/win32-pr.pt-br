---
title: Método Update da classe Win32_TSGatewayRADIUSServer
description: Atualiza o servidor atual de serviço RADIUS (RADIUS).
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayRADIUSServer, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4faf0c87e49a507ac300d7e8b32f218ed006ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644451"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="b365d-106">Método Update da classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="b365d-106">Update method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="b365d-107">Atualiza o servidor atual de serviço RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="b365d-107">Updates the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b365d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b365d-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="b365d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b365d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b365d-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b365d-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b365d-111">Nome do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b365d-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="b365d-112">*SharedSecret* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b365d-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b365d-113">Segredo compartilhado para o servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b365d-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b365d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b365d-114">Return value</span></span>

<span data-ttu-id="b365d-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b365d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b365d-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b365d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b365d-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b365d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b365d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b365d-118">Remarks</span></span>

<span data-ttu-id="b365d-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b365d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b365d-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b365d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b365d-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b365d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b365d-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b365d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b365d-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b365d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b365d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b365d-124">Requirements</span></span>



| <span data-ttu-id="b365d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b365d-125">Requirement</span></span> | <span data-ttu-id="b365d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b365d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b365d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b365d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b365d-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b365d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b365d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b365d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b365d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b365d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b365d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b365d-131">Namespace</span></span><br/>                | <span data-ttu-id="b365d-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b365d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b365d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b365d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b365d-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b365d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b365d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b365d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b365d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b365d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b365d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b365d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b365d-138">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b365d-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

