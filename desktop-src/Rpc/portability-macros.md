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
ms.openlocfilehash: 20aa6ebda92d7c3998082fdbb5e5f07aa1be22f37a6ec65a8e81327b8614565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019217"
---
# <a name="portability-macros"></a>Macros de portabilidade

As ferramentas RPC obtêm o modelo, a chamada e a independência da Convenção de nomenclatura ao associar tipos de dados e tipos de retorno de função nos arquivos stub gerados e arquivos de cabeçalho com definições específicas para cada plataforma. Essas definições de macro garantem que todos os tipos de dados e funções que exigem a designação de **\_ \_ longe** sejam especificados como objetos distantes.

A figura a seguir mostra as definições de macro que o compilador MIDL aplica a chamadas de função entre componentes RPC:

![O diagrama que mostra as definições de macro MIDL se aplica a chamadas de função.](images/prog-a29.png)

As macros RPC são definidas da seguinte maneira.



| Definição    | Descrição                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_\_API RPC  | Aplicado a chamadas feitas pelo stub para o aplicativo do usuário. Ambas as funções estão no mesmo programa executável.                                       |
| \_\_longe de RPC \_  | Aplicado à definição de macro padrão para ponteiros. Essa definição de macro deve aparecer como parte da assinatura de todas as funções fornecidas pelo usuário. |
| \_\_STUB de RPC \_ | Aplicado a chamadas feitas a partir da biblioteca de tempo de execução para o stub. Essas chamadas podem ser consideradas privadas.                                                 |
| \_\_\_usuário RPC | Aplicado a chamadas feitas pela biblioteca de tempo de execução para o aplicativo do usuário. Elas cruzam o limite entre uma DLL e um aplicativo.                   |
| \_entrada RPC    | Aplicado a chamadas feitas pelo aplicativo ou stub para a biblioteca de tempo de execução. Essa definição de macro é aplicada a todas as funções de tempo de execução RPC.           |



 

Para vincular corretamente as bibliotecas de tempo de execução, os stubs e as rotinas de suporte do Microsoft RPC, algumas funções fornecidas pelo usuário também devem incluir essas macros na definição da função. Use a **\_ \_ \_ API RPC** de macro ao definir as funções associadas com gerenciamento de memória, identificadores de associação definidos pelo usuário e o atributo **transmitir \_ como** e use o **\_ \_ \_ usuário RPC** de macro ao definir a rotina de execução de contexto associada ao identificador de contexto. Especifique as funções como:

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Alocar *\_ usuário de MIDL* de usuário RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Usuário RPC- \_ *\_ usuário de MIDL* \_ gratuito (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_ *Identificador* \_ do usuário de RPC BindType (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_ *Identificador* de usuário de RPC, \_ desassociar (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ para \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ do \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo de usuário RPC \_ para \_ transmissão (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* de usuário RPC \_ de \_ transmissão (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* de usuário RPC \_ gratuito \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Tipo* de usuário RPC \_ Free \_ Inst (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_  \_ Transmissão gratuita de tipo \_ de usuário RPC (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_ \_ Encerramento do contexto do usuário RPC (...)
</dt> <dd></dd> </dl>

> [!Note]  
> Todos os parâmetros de ponteiro nessas funções devem ser especificados usando a macro do **\_ \_ RPC para \_ longe**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



 

 





