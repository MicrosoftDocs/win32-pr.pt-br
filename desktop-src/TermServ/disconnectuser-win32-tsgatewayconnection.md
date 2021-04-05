---
title: Método DisconnectUser da classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Desconecta todas as conexões do usuário especificado do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisconnectUser
- Método DisconnectUser Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644812"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="e8a01-106">Método DisconnectUser da classe Win32 \_ TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8a01-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="e8a01-107">Desconecta todas as conexões do usuário especificado do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="e8a01-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a01-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8a01-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="e8a01-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8a01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a01-110">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8a01-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8a01-111">O nome de usuário, no formato \* DOMAIN \* **\\** _username_ , cujas conexões devem ser desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e8a01-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a01-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8a01-112">Return value</span></span>

<span data-ttu-id="e8a01-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e8a01-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e8a01-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e8a01-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e8a01-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e8a01-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8a01-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8a01-116">Remarks</span></span>

<span data-ttu-id="e8a01-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e8a01-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e8a01-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e8a01-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e8a01-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e8a01-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e8a01-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e8a01-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e8a01-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e8a01-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8a01-122">Requirements</span></span>



| <span data-ttu-id="e8a01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a01-123">Requirement</span></span> | <span data-ttu-id="e8a01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e8a01-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a01-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a01-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e8a01-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e8a01-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a01-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8a01-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="e8a01-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8a01-129">Namespace</span></span><br/>                | <span data-ttu-id="e8a01-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e8a01-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="e8a01-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8a01-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a01-132"><dt>Tsgauthenticationengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a01-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="e8a01-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e8a01-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8a01-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8a01-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="e8a01-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a01-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a01-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8a01-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="e8a01-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8a01-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a01-138">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="e8a01-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

