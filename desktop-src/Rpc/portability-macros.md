---
title: Macros de portabilidade (RPC. h)
description: As ferramentas RPC obtêm o modelo, a chamada e a independência da Convenção de nomenclatura ao associar tipos de dados e tipos de retorno de função nos arquivos stub gerados e arquivos de cabeçalho com definições específicas para cada plataforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Macros de portabilidade RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "103930075"
---
# <a name="portability-macros"></a><span data-ttu-id="d8388-104">Macros de portabilidade</span><span class="sxs-lookup"><span data-stu-id="d8388-104">Portability Macros</span></span>

<span data-ttu-id="d8388-105">As ferramentas RPC obtêm o modelo, a chamada e a independência da Convenção de nomenclatura ao associar tipos de dados e tipos de retorno de função nos arquivos stub gerados e arquivos de cabeçalho com definições específicas para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="d8388-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="d8388-106">Essas definições de macro garantem que todos os tipos de dados e funções que exigem a designação de **\_ \_ longe** sejam especificados como objetos distantes.</span><span class="sxs-lookup"><span data-stu-id="d8388-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="d8388-107">A figura a seguir mostra as definições de macro que o compilador MIDL aplica a chamadas de função entre componentes RPC:</span><span class="sxs-lookup"><span data-stu-id="d8388-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![O diagrama que mostra as definições de macro MIDL se aplica a chamadas de função.](images/prog-a29.png)

<span data-ttu-id="d8388-109">As macros RPC são definidas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d8388-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="d8388-110">Definição</span><span class="sxs-lookup"><span data-stu-id="d8388-110">Definition</span></span>    | <span data-ttu-id="d8388-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8388-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8388-112">\_\_\_API RPC</span><span class="sxs-lookup"><span data-stu-id="d8388-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="d8388-113">Aplicado a chamadas feitas pelo stub para o aplicativo do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8388-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="d8388-114">Ambas as funções estão no mesmo programa executável.</span><span class="sxs-lookup"><span data-stu-id="d8388-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="d8388-115">\_\_longe de RPC \_</span><span class="sxs-lookup"><span data-stu-id="d8388-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="d8388-116">Aplicado à definição de macro padrão para ponteiros.</span><span class="sxs-lookup"><span data-stu-id="d8388-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="d8388-117">Essa definição de macro deve aparecer como parte da assinatura de todas as funções fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d8388-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="d8388-118">\_\_STUB de RPC \_</span><span class="sxs-lookup"><span data-stu-id="d8388-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="d8388-119">Aplicado a chamadas feitas a partir da biblioteca de tempo de execução para o stub.</span><span class="sxs-lookup"><span data-stu-id="d8388-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="d8388-120">Essas chamadas podem ser consideradas privadas.</span><span class="sxs-lookup"><span data-stu-id="d8388-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="d8388-121">\_\_\_usuário RPC</span><span class="sxs-lookup"><span data-stu-id="d8388-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="d8388-122">Aplicado a chamadas feitas pela biblioteca de tempo de execução para o aplicativo do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8388-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="d8388-123">Elas cruzam o limite entre uma DLL e um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8388-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="d8388-124">\_entrada RPC</span><span class="sxs-lookup"><span data-stu-id="d8388-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="d8388-125">Aplicado a chamadas feitas pelo aplicativo ou stub para a biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d8388-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="d8388-126">Essa definição de macro é aplicada a todas as funções de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="d8388-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="d8388-127">Para vincular corretamente as bibliotecas de tempo de execução, os stubs e as rotinas de suporte do Microsoft RPC, algumas funções fornecidas pelo usuário também devem incluir essas macros na definição da função.</span><span class="sxs-lookup"><span data-stu-id="d8388-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="d8388-128">Use a **\_ \_ \_ API RPC** de macro ao definir as funções associadas com gerenciamento de memória, identificadores de associação definidos pelo usuário e o atributo **transmitir \_ como** e use o **\_ \_ \_ usuário RPC** de macro ao definir a rotina de execução de contexto associada ao identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="d8388-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="d8388-129">Especifique as funções como:</span><span class="sxs-lookup"><span data-stu-id="d8388-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="d8388-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Alocar *\_ usuário de MIDL* de usuário RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Usuário RPC- \_ *\_ usuário de MIDL* \_ gratuito (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_ *Identificador* \_ do usuário de RPC BindType (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_ *Identificador* de usuário de RPC, \_ desassociar (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ para \_ local</span><span class="sxs-lookup"><span data-stu-id="d8388-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ do \_ local</span><span class="sxs-lookup"><span data-stu-id="d8388-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo de usuário RPC \_ para \_ transmissão (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* de usuário RPC \_ de \_ transmissão (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ gratuito \_ local</span><span class="sxs-lookup"><span data-stu-id="d8388-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Tipo* de usuário RPC \_ Free \_ Inst (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_  \_ Transmissão gratuita de tipo \_ de usuário RPC (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8388-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_ \_ Encerramento do contexto do usuário RPC (...)</span><span class="sxs-lookup"><span data-stu-id="d8388-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="d8388-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d8388-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="d8388-143">Todos os parâmetros de ponteiro nessas funções devem ser especificados usando a macro do **\_ \_ RPC para \_ longe**.</span><span class="sxs-lookup"><span data-stu-id="d8388-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8388-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8388-144">Requirements</span></span>



| <span data-ttu-id="d8388-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8388-145">Requirement</span></span> | <span data-ttu-id="d8388-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d8388-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8388-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8388-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d8388-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8388-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8388-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8388-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d8388-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8388-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8388-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8388-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8388-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8388-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





