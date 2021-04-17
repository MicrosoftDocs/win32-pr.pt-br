---
title: atributo system_handle
description: O atributo \ system_handle \ especifica um tipo de identificador definido pelo sistema.
keywords:
- system_handle do atributo MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762248"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="5d488-104">atributo system_handle</span><span class="sxs-lookup"><span data-stu-id="5d488-104">system_handle attribute</span></span>

<span data-ttu-id="5d488-105">O \[  \] atributo system_handle especifica um tipo de identificador definido pelo sistema que representa o acesso a um objeto do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d488-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="5d488-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d488-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d488-107">*System-identificador-Type*</span><span class="sxs-lookup"><span data-stu-id="5d488-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5d488-108">Especifica uma das opções de tipo de identificador do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d488-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="5d488-109">As opções válidas são:</span><span class="sxs-lookup"><span data-stu-id="5d488-109">The valid options are:</span></span>
* <span data-ttu-id="5d488-110">[sh_composition](sh-composition.md) -um identificador de superfície DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5d488-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="5d488-111">[sh_event](sh-event.md) -um objeto de evento nomeado ou sem nome</span><span class="sxs-lookup"><span data-stu-id="5d488-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="5d488-112">[sh_file](sh-file.md) -um arquivo ou dispositivo de e/s</span><span class="sxs-lookup"><span data-stu-id="5d488-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="5d488-113">[sh_job](sh-job.md) -um objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="5d488-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="5d488-114">[sh_mutex](sh-mutex.md) -um objeto mutex nomeado ou sem nome</span><span class="sxs-lookup"><span data-stu-id="5d488-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="5d488-115">[sh_pipe](sh-pipe.md) -um objeto de pipe nomeado ou anônimo</span><span class="sxs-lookup"><span data-stu-id="5d488-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="5d488-116">[sh_process](sh-process.md) -um objeto de processo</span><span class="sxs-lookup"><span data-stu-id="5d488-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="5d488-117">[sh_reg_key](sh-reg-key.md) -uma chave do registro</span><span class="sxs-lookup"><span data-stu-id="5d488-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="5d488-118">[sh_section](sh-section.md) -uma seção de memória compartilhada</span><span class="sxs-lookup"><span data-stu-id="5d488-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="5d488-119">[sh_semaphore](sh-semaphore.md) -um objeto de semáforo nomeado ou sem nome</span><span class="sxs-lookup"><span data-stu-id="5d488-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="5d488-120">[sh_socket](sh-socket.md) -um objeto de soquete Winsock</span><span class="sxs-lookup"><span data-stu-id="5d488-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="5d488-121">[sh_thread](sh-thread.md) -um objeto de thread</span><span class="sxs-lookup"><span data-stu-id="5d488-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="5d488-122">[sh_token](sh-token.md) -um objeto de token de acesso</span><span class="sxs-lookup"><span data-stu-id="5d488-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="5d488-123">*opcional-máscara de acesso*</span><span class="sxs-lookup"><span data-stu-id="5d488-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="5d488-124">Opcionalmente, solicita direitos de acesso específicos aplicados ao identificador duplicado.</span><span class="sxs-lookup"><span data-stu-id="5d488-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="5d488-125">Por padrão, quando não for especificado, o identificador será duplicado com o mesmo acesso.</span><span class="sxs-lookup"><span data-stu-id="5d488-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="5d488-126">Para especificar um nível diferente de acesso, use direitos de acesso específicos do objeto correspondente ao objeto do sistema subjacente selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d488-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="5d488-127">Mais informações sobre como os direitos de acesso são propagados durante a duplicação podem ser encontradas na documentação do [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="5d488-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="5d488-128">Links para listas de direitos de acesso para cada tipo de objeto podem ser encontrados na referência *DuplicateHandle* , bem como na página **Ver também** os cabeçalhos de cada `sh_*` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d488-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d488-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d488-129">Remarks</span></span>

<span data-ttu-id="5d488-130">Para usar esse atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="5d488-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="5d488-131">Identificadores do sistema são identificadores que são definidos pelo sistema operacional para fornecer acesso a um recurso do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d488-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="5d488-132">O tipo específico do objeto por trás do identificador deve ser especificado ao declarar o atributo.</span><span class="sxs-lookup"><span data-stu-id="5d488-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="5d488-133">Para um identificador marcado `[in]` , o identificador será duplicado no procedimento remoto e permanecerá válido pela duração do procedimento.</span><span class="sxs-lookup"><span data-stu-id="5d488-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="5d488-134">No retorno do procedimento remoto, o identificador duplicado é liberado.</span><span class="sxs-lookup"><span data-stu-id="5d488-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="5d488-135">Para manter o acesso ao objeto subjacente, o aplicativo remoto deve duplicar o identificador em seu próprio espaço de endereço.</span><span class="sxs-lookup"><span data-stu-id="5d488-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="5d488-136">Por outro lado, para um identificador marcado `[out]` , quando um procedimento remoto retorna um identificador de uma chamada, o procedimento remoto perderá a propriedade dele.</span><span class="sxs-lookup"><span data-stu-id="5d488-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="5d488-137">Para manter o acesso ao objeto subjacente, o procedimento remoto deve duplicar o identificador e retornar a duplicata.</span><span class="sxs-lookup"><span data-stu-id="5d488-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="5d488-138">O identificador retornado então se torna de Propriedade do chamador que assume uma responsabilidade de fechá-lo quando o acesso ao objeto do sistema subjacente não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="5d488-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="5d488-139">Como se trata de um mecanismo para retransmitir o acesso a um objeto do sistema, esse atributo só é aplicável a chamadas entre procedimentos no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="5d488-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="5d488-140">Os parâmetros de criação e acesso fornecidos ao objeto subjacente por trás do identificador do sistema em sua criação determinarão se ele pode ser empacotado com êxito para o contexto do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="5d488-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="5d488-141">Uma matriz de `system_handle` pode ser passada para dentro ou para fora com a sintaxe encontrada na documentação do [**atributo size_is**](size-is.md) .</span><span class="sxs-lookup"><span data-stu-id="5d488-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="5d488-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d488-142">Examples</span></span>

<span data-ttu-id="5d488-143">Os exemplos a seguir são vários usos de `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="5d488-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="5d488-144">Para obter um exemplo completo, consulte o exemplo [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .</span><span class="sxs-lookup"><span data-stu-id="5d488-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="5d488-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d488-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="5d488-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d488-146">Minimum supported client</span></span> | <span data-ttu-id="5d488-147">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5d488-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="5d488-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d488-148">Minimum supported server</span></span> | <span data-ttu-id="5d488-149">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5d488-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5d488-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d488-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="5d488-151">opção /target</span><span class="sxs-lookup"><span data-stu-id="5d488-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="5d488-152">Associação e identificadores</span><span class="sxs-lookup"><span data-stu-id="5d488-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="5d488-153">Identificadores e objetos</span><span class="sxs-lookup"><span data-stu-id="5d488-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="5d488-154">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5d488-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5d488-155">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="5d488-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="5d488-156">Descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="5d488-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
