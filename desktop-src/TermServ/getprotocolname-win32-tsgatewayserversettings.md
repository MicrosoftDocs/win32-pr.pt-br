---
title: Método getprotocolname da classe Win32_TSGatewayServerSettings
description: Retorna o nome do protocolo para o índice de protocolo especificado.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Método getprotocolname Serviços de Área de Trabalho Remota
- Método getprotocolname Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método getprotocolname
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085773"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="fd918-106">Método getprotocolname da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="fd918-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fd918-107">Retorna o nome do protocolo para o índice de protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="fd918-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd918-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd918-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="fd918-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd918-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd918-110">*Protocolid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd918-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd918-111">Índice do identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="fd918-111">Index of the protocol identifier.</span></span> <span data-ttu-id="fd918-112">O valor deve estar entre zero e o valor da propriedade **MaxProtocols** .</span><span class="sxs-lookup"><span data-stu-id="fd918-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="fd918-113">*ProtocolName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd918-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd918-114">Retorna o nome do protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="fd918-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd918-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd918-115">Return value</span></span>

<span data-ttu-id="fd918-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fd918-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fd918-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fd918-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fd918-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fd918-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd918-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd918-119">Remarks</span></span>

<span data-ttu-id="fd918-120">Há suporte para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="fd918-120">One protocol is supported.</span></span>

<span data-ttu-id="fd918-121">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="fd918-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fd918-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fd918-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd918-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fd918-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd918-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fd918-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd918-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd918-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd918-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd918-126">Requirements</span></span>



| <span data-ttu-id="fd918-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd918-127">Requirement</span></span> | <span data-ttu-id="fd918-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fd918-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd918-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd918-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd918-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fd918-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fd918-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd918-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd918-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd918-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fd918-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd918-133">Namespace</span></span><br/>                | <span data-ttu-id="fd918-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fd918-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fd918-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fd918-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd918-136"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd918-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd918-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fd918-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd918-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd918-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fd918-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd918-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd918-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="fd918-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

