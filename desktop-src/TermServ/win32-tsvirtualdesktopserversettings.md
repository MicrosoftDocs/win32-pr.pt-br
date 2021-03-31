---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contém informações de configuração para um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVirtualDesktopServerSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVirtualDesktopServerSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645091"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="70b6a-105">\_Classe Win32 TSVirtualDesktopServerSettings</span><span class="sxs-lookup"><span data-stu-id="70b6a-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="70b6a-106">Contém informações de configuração para um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).</span><span class="sxs-lookup"><span data-stu-id="70b6a-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="70b6a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="70b6a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b6a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70b6a-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="70b6a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="70b6a-109">Members</span></span>

<span data-ttu-id="70b6a-110">A classe **Win32 \_ TSVirtualDesktopServerSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="70b6a-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="70b6a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70b6a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70b6a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70b6a-112">Properties</span></span>

<span data-ttu-id="70b6a-113">A classe **Win32 \_ TSVirtualDesktopServerSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="70b6a-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70b6a-114">**Simultaneidade**</span><span class="sxs-lookup"><span data-stu-id="70b6a-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b6a-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70b6a-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70b6a-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70b6a-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="70b6a-117">O máximo permitido de solicitações simultâneas de provisionamento para este servidor de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="70b6a-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="70b6a-118">**PolicySourceSessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="70b6a-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b6a-119">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="70b6a-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="70b6a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70b6a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b6a-121">Se definido como 0, indica que a propriedade **SessionBrokerName** está configurada pelo servidor; Se definido como 1, indica que a propriedade **SessionBrokerName** é configurada por uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="70b6a-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="70b6a-122">**SessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="70b6a-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b6a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70b6a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b6a-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70b6a-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="70b6a-125">O nome distinto totalmente qualificado do agente de sessão para o servidor de host de virtualização de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="70b6a-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70b6a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70b6a-126">Requirements</span></span>



| <span data-ttu-id="70b6a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b6a-127">Requirement</span></span> | <span data-ttu-id="70b6a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="70b6a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b6a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70b6a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="70b6a-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="70b6a-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="70b6a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70b6a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="70b6a-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70b6a-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="70b6a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="70b6a-133">Namespace</span></span><br/>                | <span data-ttu-id="70b6a-134">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="70b6a-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="70b6a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="70b6a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70b6a-136"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70b6a-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="70b6a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="70b6a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b6a-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70b6a-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





