---
title: Classe Win32_TSGatewayServer
description: Usado para operações específicas de servidor do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455035"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="c99f4-105">\_Classe Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="c99f4-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="c99f4-106">Usado para operações específicas de servidor do gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="c99f4-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c99f4-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="c99f4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c99f4-108">Members</span></span>

<span data-ttu-id="c99f4-109">A classe **Win32 \_ TSGatewayServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c99f4-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="c99f4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c99f4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c99f4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c99f4-111">Methods</span></span>

<span data-ttu-id="c99f4-112">A classe **Win32 \_ TSGatewayServer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c99f4-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="c99f4-113">Método</span><span class="sxs-lookup"><span data-stu-id="c99f4-113">Method</span></span>                                                                                   | <span data-ttu-id="c99f4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c99f4-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c99f4-115">**CreateSelfSignedCertificate**</span><span class="sxs-lookup"><span data-stu-id="c99f4-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="c99f4-116">Cria um certificado autoassinado com um determinado nome de entidade e retorna o hash de certificado como um parâmetro "out".</span><span class="sxs-lookup"><span data-stu-id="c99f4-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="c99f4-117">**Exportação**</span><span class="sxs-lookup"><span data-stu-id="c99f4-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="c99f4-118">Retorna a configuração do servidor de gateway de área de trabalho remota como uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="c99f4-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="c99f4-119">**Importar**</span><span class="sxs-lookup"><span data-stu-id="c99f4-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="c99f4-120">Importa uma determinada configuração para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="c99f4-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="c99f4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c99f4-121">Remarks</span></span>

<span data-ttu-id="c99f4-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c99f4-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c99f4-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c99f4-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c99f4-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c99f4-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c99f4-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c99f4-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c99f4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c99f4-126">Requirements</span></span>



| <span data-ttu-id="c99f4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99f4-127">Requirement</span></span> | <span data-ttu-id="c99f4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c99f4-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c99f4-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c99f4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c99f4-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c99f4-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c99f4-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c99f4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c99f4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c99f4-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c99f4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c99f4-133">Namespace</span></span><br/>                | <span data-ttu-id="c99f4-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c99f4-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c99f4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c99f4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c99f4-136"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c99f4-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c99f4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c99f4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c99f4-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c99f4-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

