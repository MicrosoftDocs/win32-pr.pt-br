---
description: 'O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para consultar ou modificar o banco de dados dos serviços instalados. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:'
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configurando um serviço usando SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756370"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="87f8f-105">Configurando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="87f8f-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="87f8f-106">O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para consultar ou modificar o banco de dados dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="87f8f-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="87f8f-107">Seus comandos correspondem às funções fornecidas pelo SCM.</span><span class="sxs-lookup"><span data-stu-id="87f8f-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="87f8f-108">A sintaxe é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="87f8f-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f8f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="87f8f-109">Syntax</span></span>

<span data-ttu-id="87f8f-110">**SC** \[ *Nome do Server* \] *Comando* \[ *ServiceName* \] \[  \] opção 1 \[ *opção 2* \] ...</span><span class="sxs-lookup"><span data-stu-id="87f8f-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="87f8f-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="87f8f-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="87f8f-112">Nome do servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="87f8f-112">Optional server name.</span></span> <span data-ttu-id="87f8f-113">Use o formulário \\ \\ *nomedoservidor*.</span><span class="sxs-lookup"><span data-stu-id="87f8f-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="87f8f-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Linha*</span><span class="sxs-lookup"><span data-stu-id="87f8f-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="87f8f-115">Um dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="87f8f-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="87f8f-116">boot</span><span class="sxs-lookup"><span data-stu-id="87f8f-116">boot</span></span></dd> <dd><span data-ttu-id="87f8f-117">config</span><span class="sxs-lookup"><span data-stu-id="87f8f-117">config</span></span></dd> <dd><span data-ttu-id="87f8f-118">create</span><span class="sxs-lookup"><span data-stu-id="87f8f-118">create</span></span></dd> <dd><span data-ttu-id="87f8f-119">excluir</span><span class="sxs-lookup"><span data-stu-id="87f8f-119">delete</span></span></dd> <dd><span data-ttu-id="87f8f-120">descrição</span><span class="sxs-lookup"><span data-stu-id="87f8f-120">description</span></span></dd> <dd><span data-ttu-id="87f8f-121">EnumDepend</span><span class="sxs-lookup"><span data-stu-id="87f8f-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="87f8f-122">falha</span><span class="sxs-lookup"><span data-stu-id="87f8f-122">failure</span></span></dd> <dd><span data-ttu-id="87f8f-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="87f8f-123">failureflag</span></span></dd> <dd><span data-ttu-id="87f8f-124">GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="87f8f-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="87f8f-125">GetKeyName</span><span class="sxs-lookup"><span data-stu-id="87f8f-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="87f8f-126">Bloqueio</span><span class="sxs-lookup"><span data-stu-id="87f8f-126">Lock</span></span></dd> <dd><span data-ttu-id="87f8f-127">qc</span><span class="sxs-lookup"><span data-stu-id="87f8f-127">qc</span></span></dd> <dd><span data-ttu-id="87f8f-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="87f8f-128">qdescription</span></span></dd> <dd><span data-ttu-id="87f8f-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="87f8f-129">qfailure</span></span></dd> <dd><span data-ttu-id="87f8f-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="87f8f-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="87f8f-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="87f8f-131">qprivs</span></span></dd> <dd><span data-ttu-id="87f8f-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="87f8f-132">qsidtype</span></span></dd> <dd><span data-ttu-id="87f8f-133">Consulta</span><span class="sxs-lookup"><span data-stu-id="87f8f-133">query</span></span></dd> <dd><span data-ttu-id="87f8f-134">QueryEx</span><span class="sxs-lookup"><span data-stu-id="87f8f-134">queryex</span></span></dd> <dd><span data-ttu-id="87f8f-135">privs</span><span class="sxs-lookup"><span data-stu-id="87f8f-135">privs</span></span></dd> <dd><span data-ttu-id="87f8f-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="87f8f-136">QueryLock</span></span></dd> <dd><span data-ttu-id="87f8f-137">sdset</span><span class="sxs-lookup"><span data-stu-id="87f8f-137">sdset</span></span></dd> <dd><span data-ttu-id="87f8f-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="87f8f-138">sdshow</span></span></dd> <dd><span data-ttu-id="87f8f-139">showsid</span><span class="sxs-lookup"><span data-stu-id="87f8f-139">showsid</span></span></dd> <dd><span data-ttu-id="87f8f-140">sidtype</span><span class="sxs-lookup"><span data-stu-id="87f8f-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="87f8f-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="87f8f-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="87f8f-142">O nome do serviço, conforme especificado quando ele foi instalado.</span><span class="sxs-lookup"><span data-stu-id="87f8f-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="87f8f-143"><span id="option1"></span><span id="OPTION1"></span>*opção 1*</span><span class="sxs-lookup"><span data-stu-id="87f8f-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="87f8f-144">Um parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="87f8f-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="87f8f-145"><span id="option2"></span><span id="OPTION2"></span>*opção 2*</span><span class="sxs-lookup"><span data-stu-id="87f8f-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="87f8f-146">Um parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="87f8f-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87f8f-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="87f8f-147">Remarks</span></span>

<span data-ttu-id="87f8f-148">Para ver a sintaxe completa de um comando, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="87f8f-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="87f8f-149"> *comando* SC</span><span class="sxs-lookup"><span data-stu-id="87f8f-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="87f8f-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87f8f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f8f-151">Configuração do serviço</span><span class="sxs-lookup"><span data-stu-id="87f8f-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="87f8f-152">Instalação, remoção e enumeração de serviço</span><span class="sxs-lookup"><span data-stu-id="87f8f-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



