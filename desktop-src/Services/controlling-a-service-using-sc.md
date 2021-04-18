---
description: 'O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:'
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlando um serviço usando SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755948"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="00218-105">Controlando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="00218-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="00218-106">O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço.</span><span class="sxs-lookup"><span data-stu-id="00218-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="00218-107">Seus comandos correspondem às funções fornecidas pelo SCM.</span><span class="sxs-lookup"><span data-stu-id="00218-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="00218-108">A sintaxe é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="00218-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="00218-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00218-109">Syntax</span></span>

<span data-ttu-id="00218-110">**SC** \[ *Nome do Server* \] *Comando* \[ *ServiceName* \] \[  \] opção 1 \[ *opção 2* \] ...</span><span class="sxs-lookup"><span data-stu-id="00218-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="00218-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="00218-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="00218-112">Nome do servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="00218-112">Optional server name.</span></span> <span data-ttu-id="00218-113">Use o formulário \\ \\ *nomedoservidor*.</span><span class="sxs-lookup"><span data-stu-id="00218-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="00218-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Linha*</span><span class="sxs-lookup"><span data-stu-id="00218-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="00218-115">Um dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="00218-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="00218-116">continue</span><span class="sxs-lookup"><span data-stu-id="00218-116">continue</span></span></dd> <dd><span data-ttu-id="00218-117">controle</span><span class="sxs-lookup"><span data-stu-id="00218-117">control</span></span></dd> <dd><span data-ttu-id="00218-118">interrogar</span><span class="sxs-lookup"><span data-stu-id="00218-118">interrogate</span></span></dd> <dd><span data-ttu-id="00218-119">pause</span><span class="sxs-lookup"><span data-stu-id="00218-119">pause</span></span></dd> <dd><span data-ttu-id="00218-120">iniciar</span><span class="sxs-lookup"><span data-stu-id="00218-120">start</span></span></dd> <dd><span data-ttu-id="00218-121">parar</span><span class="sxs-lookup"><span data-stu-id="00218-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="00218-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="00218-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="00218-123">O nome do serviço, conforme especificado quando ele foi instalado.</span><span class="sxs-lookup"><span data-stu-id="00218-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="00218-124"><span id="option1"></span><span id="OPTION1"></span>*opção 1*</span><span class="sxs-lookup"><span data-stu-id="00218-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="00218-125">Um parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="00218-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="00218-126"><span id="option2"></span><span id="OPTION2"></span>*opção 2*</span><span class="sxs-lookup"><span data-stu-id="00218-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="00218-127">Um parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="00218-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00218-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="00218-128">Remarks</span></span>

<span data-ttu-id="00218-129">Para ver a sintaxe completa de um comando, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="00218-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="00218-130"> *comando* SC</span><span class="sxs-lookup"><span data-stu-id="00218-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="00218-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00218-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00218-132">Solicitações de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="00218-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="00218-133">Inicialização do serviço</span><span class="sxs-lookup"><span data-stu-id="00218-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



