---
title: Objeto Session (WSManDisp. h)
description: Define as configurações de operações e de sessão.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de objeto de sessão
- Gerenciamento Remoto do Windows de objeto de sessão, descrito
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919201"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="fafb3-105">Objeto Session (WSManDisp. h)</span><span class="sxs-lookup"><span data-stu-id="fafb3-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="fafb3-106">Define as configurações de operações e de sessão.</span><span class="sxs-lookup"><span data-stu-id="fafb3-106">Defines operations and session settings.</span></span> <span data-ttu-id="fafb3-107">Todas as operações de Gerenciamento Remoto do Windows exigem a criação de uma **sessão** que se conecta a um computador remoto, BMC ( [*controlador de gerenciamento base*](windows-remote-management-glossary.md) ) ou o computador local.</span><span class="sxs-lookup"><span data-stu-id="fafb3-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="fafb3-108">As operações de rede do WinRM incluem obter, gravar ou enumerar dados ou invocar métodos.</span><span class="sxs-lookup"><span data-stu-id="fafb3-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="fafb3-109">Os métodos do objeto de **sessão** espelham as operações básicas definidas no protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="fafb3-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="fafb3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fafb3-110">Members</span></span>

<span data-ttu-id="fafb3-111">O objeto de **sessão** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fafb3-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="fafb3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fafb3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fafb3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fafb3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fafb3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fafb3-114">Methods</span></span>

<span data-ttu-id="fafb3-115">O objeto de **sessão** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fafb3-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="fafb3-116">Método</span><span class="sxs-lookup"><span data-stu-id="fafb3-116">Method</span></span>                                 | <span data-ttu-id="fafb3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fafb3-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fafb3-118">**Criada**</span><span class="sxs-lookup"><span data-stu-id="fafb3-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="fafb3-119">Cria uma nova instância de um recurso e retorna o URI do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="fafb3-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="fafb3-120">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="fafb3-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="fafb3-121">Exclui o recurso especificado no URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="fafb3-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="fafb3-122">**Enumerar**</span><span class="sxs-lookup"><span data-stu-id="fafb3-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="fafb3-123">Enumera um recurso de coleta, tabela ou log de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fafb3-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="fafb3-124">**Obter**</span><span class="sxs-lookup"><span data-stu-id="fafb3-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="fafb3-125">Recupera um recurso do serviço e retorna uma representação XML da instância atual do recurso.</span><span class="sxs-lookup"><span data-stu-id="fafb3-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="fafb3-126">**Identificar**</span><span class="sxs-lookup"><span data-stu-id="fafb3-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="fafb3-127">Consulta um computador remoto para determinar se ele dá suporte ao protocolo de WS-Management</span><span class="sxs-lookup"><span data-stu-id="fafb3-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="fafb3-128">**Chame**</span><span class="sxs-lookup"><span data-stu-id="fafb3-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="fafb3-129">Invoca um método que retorna os resultados da chamada de método.</span><span class="sxs-lookup"><span data-stu-id="fafb3-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="fafb3-130">**Posicione**</span><span class="sxs-lookup"><span data-stu-id="fafb3-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="fafb3-131">Atualiza um recurso.</span><span class="sxs-lookup"><span data-stu-id="fafb3-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="fafb3-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fafb3-132">Properties</span></span>

<span data-ttu-id="fafb3-133">O objeto de **sessão** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fafb3-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="fafb3-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fafb3-134">Property</span></span>                                            | <span data-ttu-id="fafb3-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fafb3-135">Access type</span></span>           | <span data-ttu-id="fafb3-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="fafb3-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fafb3-137">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="fafb3-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="fafb3-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fafb3-138">Read/write</span></span><br/> | <span data-ttu-id="fafb3-139">Define e Obtém o número de itens em cada lote de enumeração.</span><span class="sxs-lookup"><span data-stu-id="fafb3-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="fafb3-140">Esse valor não pode ser alterado durante uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="fafb3-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="fafb3-141">Por padrão, o padrão é um número ilimitado de itens.</span><span class="sxs-lookup"><span data-stu-id="fafb3-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="fafb3-142">O provedor de recursos pode definir um limite.</span><span class="sxs-lookup"><span data-stu-id="fafb3-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="fafb3-143">**Erro**</span><span class="sxs-lookup"><span data-stu-id="fafb3-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="fafb3-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fafb3-144">Read-only</span></span><br/>  | <span data-ttu-id="fafb3-145">Obtém informações de erro adicionais em um fluxo XML.</span><span class="sxs-lookup"><span data-stu-id="fafb3-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="fafb3-146">**Cedido**</span><span class="sxs-lookup"><span data-stu-id="fafb3-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="fafb3-147">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fafb3-147">Read/write</span></span><br/> | <span data-ttu-id="fafb3-148">Define e obtém a quantidade máxima de tempo (em milissegundos) para o aplicativo cliente aguardar.</span><span class="sxs-lookup"><span data-stu-id="fafb3-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="fafb3-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="fafb3-149">Remarks</span></span>

<span data-ttu-id="fafb3-150">O objeto de **sessão** corresponde à interface [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .</span><span class="sxs-lookup"><span data-stu-id="fafb3-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="fafb3-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fafb3-151">Examples</span></span>

<span data-ttu-id="fafb3-152">O exemplo de código VBScript a seguir mostra como criar um objeto de **sessão** .</span><span class="sxs-lookup"><span data-stu-id="fafb3-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="fafb3-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fafb3-153">Requirements</span></span>



| <span data-ttu-id="fafb3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="fafb3-154">Requirement</span></span> | <span data-ttu-id="fafb3-155">Valor</span><span class="sxs-lookup"><span data-stu-id="fafb3-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fafb3-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafb3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="fafb3-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fafb3-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fafb3-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafb3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="fafb3-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fafb3-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fafb3-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fafb3-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafb3-161"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fafb3-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fafb3-162">INSERI</span><span class="sxs-lookup"><span data-stu-id="fafb3-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fafb3-163"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fafb3-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fafb3-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fafb3-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="fafb3-165"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fafb3-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fafb3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="fafb3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafb3-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafb3-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fafb3-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="fafb3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafb3-169">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="fafb3-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="fafb3-170">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="fafb3-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fafb3-171">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="fafb3-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fafb3-172">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="fafb3-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fafb3-173">Obtendo dados do computador local</span><span class="sxs-lookup"><span data-stu-id="fafb3-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="fafb3-174">Obtendo dados de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="fafb3-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





