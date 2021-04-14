---
title: Método SetSslBridging da classe Win32_TSGatewayServerSettings
description: Define o tipo de ponte SSL a ser usado pelo servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSslBridging
- Método SetSslBridging Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369720"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="cfdc0-106">Método SetSslBridging da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="cfdc0-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="cfdc0-107">Define o tipo de ponte SSL a ser usado pelo servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="cfdc0-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="cfdc0-108">Esse valor é armazenado na propriedade **SslBridging** .</span><span class="sxs-lookup"><span data-stu-id="cfdc0-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfdc0-109">Quando o tipo de ponte SSL é alterado com esse método, o serviço de gateway de área de trabalho remota deve ser reiniciado para fazer com que essa alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cfdc0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfdc0-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="cfdc0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfdc0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfdc0-112">*SslBridging* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfdc0-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfdc0-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfdc0-113">Type: **uint32**</span></span>

<span data-ttu-id="cfdc0-114">Especifica o novo valor de ponte SSL.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="cfdc0-115">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="cfdc0-116">0</span><span class="sxs-lookup"><span data-stu-id="cfdc0-116">0</span></span>
</dt> <dd>

<span data-ttu-id="cfdc0-117">Sem ponte SSL.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="cfdc0-118">1</span><span class="sxs-lookup"><span data-stu-id="cfdc0-118">1</span></span>
</dt> <dd>

<span data-ttu-id="cfdc0-119">Conexão HTTPS com HTTP.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="cfdc0-120">2</span><span class="sxs-lookup"><span data-stu-id="cfdc0-120">2</span></span>
</dt> <dd>

<span data-ttu-id="cfdc0-121">Conexão HTTPS com HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfdc0-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfdc0-122">Return value</span></span>

<span data-ttu-id="cfdc0-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfdc0-123">Type: **uint32**</span></span>

<span data-ttu-id="cfdc0-124">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cfdc0-125">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cfdc0-126">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cfdc0-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfdc0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfdc0-127">Remarks</span></span>

<span data-ttu-id="cfdc0-128">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cfdc0-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cfdc0-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cfdc0-130">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cfdc0-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="cfdc0-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cfdc0-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cfdc0-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfdc0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfdc0-133">Requirements</span></span>



| <span data-ttu-id="cfdc0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfdc0-134">Requirement</span></span> | <span data-ttu-id="cfdc0-135">Valor</span><span class="sxs-lookup"><span data-stu-id="cfdc0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfdc0-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfdc0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdc0-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cfdc0-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cfdc0-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfdc0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdc0-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfdc0-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="cfdc0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfdc0-140">Namespace</span></span><br/>                | <span data-ttu-id="cfdc0-141">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="cfdc0-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cfdc0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cfdc0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfdc0-143"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfdc0-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfdc0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cfdc0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfdc0-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfdc0-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cfdc0-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfdc0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdc0-147">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="cfdc0-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

