---
title: Classe Win32_SessionDirectoryVirtualDesktopServer
description: Representa um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD) que ingressou em um agente de sessão.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryVirtualDesktopServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryVirtualDesktopServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009086"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="b95c0-105">\_Classe Win32 SessionDirectoryVirtualDesktopServer</span><span class="sxs-lookup"><span data-stu-id="b95c0-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="b95c0-106">Representa um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD) que ingressou em um agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="b95c0-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="b95c0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b95c0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95c0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b95c0-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b95c0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b95c0-109">Members</span></span>

<span data-ttu-id="b95c0-110">A classe **Win32 \_ SessionDirectoryVirtualDesktopServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b95c0-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="b95c0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b95c0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b95c0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b95c0-112">Properties</span></span>

<span data-ttu-id="b95c0-113">A classe **Win32 \_ SessionDirectoryVirtualDesktopServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b95c0-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b95c0-114">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b95c0-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b95c0-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b95c0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b95c0-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b95c0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b95c0-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b95c0-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b95c0-118">O nome DNS do servidor host de virtualização de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="b95c0-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="b95c0-119">Esse nome assume o formato "*MachineName*. *Domain*. com ".</span><span class="sxs-lookup"><span data-stu-id="b95c0-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b95c0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b95c0-120">Requirements</span></span>



| <span data-ttu-id="b95c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b95c0-121">Requirement</span></span> | <span data-ttu-id="b95c0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b95c0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b95c0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b95c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b95c0-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b95c0-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b95c0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b95c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b95c0-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b95c0-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b95c0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b95c0-127">Namespace</span></span><br/>                | <span data-ttu-id="b95c0-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b95c0-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b95c0-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b95c0-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b95c0-130"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b95c0-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b95c0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b95c0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b95c0-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b95c0-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

