---
title: Método SetSharedSecret da classe Win32_TSGatewayRADIUSServer
description: Define a propriedade SharedSecret para este servidor de serviço RADIUS (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSharedSecret
- Método SetSharedSecret Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota, método SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644866"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="7854c-106">Método SetSharedSecret da classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="7854c-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="7854c-107">Define a propriedade **SharedSecret** para este servidor de serviço RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="7854c-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7854c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7854c-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="7854c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7854c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7854c-110">*SharedSecret* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7854c-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7854c-111">Novo segredo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7854c-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7854c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7854c-112">Return value</span></span>

<span data-ttu-id="7854c-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7854c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7854c-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7854c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7854c-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7854c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7854c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7854c-116">Remarks</span></span>

<span data-ttu-id="7854c-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7854c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7854c-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7854c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7854c-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7854c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7854c-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7854c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7854c-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7854c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7854c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7854c-122">Requirements</span></span>



| <span data-ttu-id="7854c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7854c-123">Requirement</span></span> | <span data-ttu-id="7854c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7854c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7854c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7854c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7854c-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7854c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7854c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7854c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7854c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7854c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7854c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7854c-129">Namespace</span></span><br/>                | <span data-ttu-id="7854c-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7854c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7854c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7854c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7854c-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7854c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7854c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7854c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7854c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7854c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7854c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7854c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7854c-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="7854c-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

