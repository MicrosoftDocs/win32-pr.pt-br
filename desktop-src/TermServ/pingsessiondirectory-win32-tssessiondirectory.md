---
title: Método PingSessionDirectory da classe Win32_TSSessionDirectory
description: Verifica se o servidor do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) está disponível.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método PingSessionDirectory
- Método PingSessionDirectory Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499462"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="b2d70-106">Método PingSessionDirectory da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="b2d70-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="b2d70-107">Verifica se o servidor do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) está disponível.</span><span class="sxs-lookup"><span data-stu-id="b2d70-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d70-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2d70-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="b2d70-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2d70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d70-110">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2d70-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d70-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2d70-111">Type: **string**</span></span>

<span data-ttu-id="b2d70-112">Nome do servidor do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="b2d70-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d70-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2d70-113">Return value</span></span>

<span data-ttu-id="b2d70-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2d70-114">Type: **uint32**</span></span>

<span data-ttu-id="b2d70-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="b2d70-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b2d70-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="b2d70-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d70-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2d70-117">Remarks</span></span>

<span data-ttu-id="b2d70-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b2d70-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b2d70-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d70-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b2d70-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b2d70-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b2d70-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b2d70-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d70-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2d70-122">Requirements</span></span>



| <span data-ttu-id="b2d70-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2d70-123">Requirement</span></span> | <span data-ttu-id="b2d70-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b2d70-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d70-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2d70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d70-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b2d70-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b2d70-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2d70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d70-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2d70-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2d70-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2d70-129">Namespace</span></span><br/>                | <span data-ttu-id="b2d70-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b2d70-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b2d70-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b2d70-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2d70-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2d70-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2d70-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b2d70-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2d70-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2d70-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d70-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2d70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d70-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="b2d70-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

