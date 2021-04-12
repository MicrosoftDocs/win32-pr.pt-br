---
title: Método ITSRemoteProgram ServerStartProgram
description: Especifica um programa do RemoteApp para iniciar na sessão remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram, método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram2
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram2, método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, método ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499463"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="e6027-110">Método ITSRemoteProgram:: ServerStartProgram</span><span class="sxs-lookup"><span data-stu-id="e6027-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="e6027-111">Especifica um programa do RemoteApp para iniciar na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="e6027-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="e6027-112">Essa função deve ser invocada em uma sessão conectada (depois que a notificação de sessão conectada for recebida no cliente).</span><span class="sxs-lookup"><span data-stu-id="e6027-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="e6027-113">Qualquer número de programas do RemoteApp pode ser iniciado em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e6027-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="e6027-114">Uma sessão do RemoteApp atingirá o tempo limite se nenhum programa do RemoteApp for iniciado na sessão dentro do limite de tempo limite, que é de dois minutos para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e6027-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6027-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6027-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="e6027-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6027-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6027-117">*bstrExecutablePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-118">O caminho do arquivo executável do programa do RemoteApp no servidor.</span><span class="sxs-lookup"><span data-stu-id="e6027-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="e6027-119">*bstrFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-120">O caminho de um arquivo a ser aberto no servidor por meio de uma associação de arquivo, por exemplo, "C: \\ \\ documents \\ \\MyReport.docx".</span><span class="sxs-lookup"><span data-stu-id="e6027-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="e6027-121">Se você especificar *bstrFilePath*, não deverá especificar o parâmetro *bstrExecutablePath* e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="e6027-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="e6027-122">Você deve especificar apenas um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6027-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="e6027-123">*bstrWorkingDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-124">O diretório de trabalho no servidor para o programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e6027-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="e6027-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-126">Indica se o servidor deve expandir as variáveis de ambiente no caminho do diretório de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6027-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="e6027-127">Defina esse parâmetro como **Variant \_ true** se o caminho do diretório de trabalho contiver variáveis de ambiente ou **Variant \_ false** se o caminho do diretório de trabalho não contiver variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="e6027-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="e6027-128">*bstrArguments* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-129">Os argumentos de linha de comando para o programa RemoteApp que são especificados em *bstrExecutablePath*.</span><span class="sxs-lookup"><span data-stu-id="e6027-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="e6027-130">Defina como **NULL** se *bstrExecutablePath* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="e6027-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="e6027-131">*vbExpandEnvVarInArgumentsOnServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6027-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6027-132">Indica se o servidor deve expandir as variáveis de ambiente nos argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e6027-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="e6027-133">Defina esse parâmetro como **Variant \_ true** se os argumentos contiverem variáveis de ambiente ou **Variant \_ false** se os argumentos não contiverem variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="e6027-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6027-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6027-134">Return value</span></span>

<span data-ttu-id="e6027-135">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e6027-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6027-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6027-136">Requirements</span></span>



| <span data-ttu-id="e6027-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6027-137">Requirement</span></span> | <span data-ttu-id="e6027-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e6027-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6027-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6027-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e6027-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6027-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6027-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6027-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e6027-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6027-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6027-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e6027-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6027-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6027-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6027-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e6027-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6027-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6027-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6027-147">IID</span><span class="sxs-lookup"><span data-stu-id="e6027-147">IID</span></span><br/>                      | <span data-ttu-id="e6027-148">IID \_ ITSRemoteProgram é definido como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="e6027-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="e6027-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6027-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6027-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="e6027-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="e6027-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="e6027-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="e6027-152">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="e6027-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





