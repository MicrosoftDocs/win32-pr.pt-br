---
title: Interface ITSRemoteProgram
description: Inclui métodos para definir e recuperar o modo RemoteApp e os parâmetros de inicialização para um programa RemoteApp, como o caminho do arquivo executável e o diretório de trabalho.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota da interface ITSRemoteProgram, descrita
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009509"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="c1f50-105">Interface ITSRemoteProgram</span><span class="sxs-lookup"><span data-stu-id="c1f50-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="c1f50-106">Inclui métodos para definir e recuperar o modo RemoteApp e os parâmetros de inicialização para um programa RemoteApp, como o caminho do arquivo executável e o diretório de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1f50-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="c1f50-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c1f50-107">Members</span></span>

<span data-ttu-id="c1f50-108">A interface **ITSRemoteProgram** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c1f50-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c1f50-109">**ITSRemoteProgram** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1f50-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="c1f50-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1f50-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1f50-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1f50-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1f50-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1f50-112">Methods</span></span>

<span data-ttu-id="c1f50-113">A interface **ITSRemoteProgram** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1f50-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="c1f50-114">Método</span><span class="sxs-lookup"><span data-stu-id="c1f50-114">Method</span></span>                                                            | <span data-ttu-id="c1f50-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1f50-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="c1f50-116">**ServerStartProgram**</span><span class="sxs-lookup"><span data-stu-id="c1f50-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="c1f50-117">Especifica um programa do RemoteApp para iniciar na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="c1f50-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c1f50-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1f50-118">Properties</span></span>

<span data-ttu-id="c1f50-119">A interface **ITSRemoteProgram** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1f50-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="c1f50-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c1f50-120">Property</span></span>                                                                   | <span data-ttu-id="c1f50-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c1f50-121">Access type</span></span>           | <span data-ttu-id="c1f50-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1f50-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="c1f50-123">**RemoteProgramMode**</span><span class="sxs-lookup"><span data-stu-id="c1f50-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="c1f50-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c1f50-124">Read/write</span></span><br/> | <span data-ttu-id="c1f50-125">O modo do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c1f50-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1f50-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1f50-126">Requirements</span></span>



| <span data-ttu-id="c1f50-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1f50-127">Requirement</span></span> | <span data-ttu-id="c1f50-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c1f50-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f50-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1f50-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f50-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1f50-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c1f50-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1f50-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f50-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1f50-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c1f50-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c1f50-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1f50-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f50-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1f50-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f50-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1f50-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f50-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1f50-137">IID</span><span class="sxs-lookup"><span data-stu-id="c1f50-137">IID</span></span><br/>                      | <span data-ttu-id="c1f50-138">IID \_ ITSRemoteProgram é definido como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="c1f50-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="c1f50-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1f50-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f50-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c1f50-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c1f50-141">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="c1f50-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

