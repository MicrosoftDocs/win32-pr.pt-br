---
title: Método TSGStoreConsentMsg da classe Win32_TSGatewayServerSettings
description: Atualiza a mensagem de consentimento para o servidor de gateway.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método TSGStoreConsentMsg
- Método TSGStoreConsentMsg Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método TSGStoreConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455271"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b90e2-106">Método TSGStoreConsentMsg da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="b90e2-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b90e2-107">Atualiza a mensagem de consentimento para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="b90e2-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90e2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b90e2-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="b90e2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b90e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90e2-110">*TSGConMsgText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b90e2-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90e2-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b90e2-111">Type: **string**</span></span>

<span data-ttu-id="b90e2-112">O texto da mensagem de consentimento.</span><span class="sxs-lookup"><span data-stu-id="b90e2-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b90e2-113">Return value</span></span>

<span data-ttu-id="b90e2-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b90e2-114">Type: **uint32**</span></span>

<span data-ttu-id="b90e2-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b90e2-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b90e2-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b90e2-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b90e2-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b90e2-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b90e2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b90e2-118">Remarks</span></span>

<span data-ttu-id="b90e2-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b90e2-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b90e2-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b90e2-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b90e2-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b90e2-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b90e2-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b90e2-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b90e2-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b90e2-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b90e2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b90e2-124">Requirements</span></span>



| <span data-ttu-id="b90e2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b90e2-125">Requirement</span></span> | <span data-ttu-id="b90e2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b90e2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90e2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b90e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b90e2-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b90e2-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b90e2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b90e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b90e2-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b90e2-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b90e2-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b90e2-131">Namespace</span></span><br/>                | <span data-ttu-id="b90e2-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b90e2-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b90e2-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b90e2-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b90e2-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b90e2-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b90e2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b90e2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b90e2-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b90e2-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b90e2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b90e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90e2-138">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b90e2-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

