---
title: Classe MSAD_ReplPendingOp
description: Representa a \_ estrutura de op de repl DS \_ , que descreve uma tarefa de replicação que está atualmente em execução ou com execução pendente.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_ReplPendingOp Active Directory
- Active Directory de MSAD_ReplPendingOp classe, descrita
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369627"
---
# <a name="msad_replpendingop-class"></a>\_Classe MSAD ReplPendingOp

Representa a estrutura de [**\_ \_ op de repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , que descreve uma tarefa de replicação que está atualmente em execução ou com execução pendente. Essa estrutura é retornada pela função [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>Membros

A classe **MSAD \_ ReplPendingOp** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSAD \_ ReplPendingOp** tem essas propriedades.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o endereço de rede específico de transporte do servidor remoto que está associado a esta operação. **NULL** se não houver um servidor remoto associado a esta operação.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o caminho X. 500 do DSA associado ao servidor remoto que corresponde a essa operação. **NULL** se nenhum servidor remoto corresponder a esta operação.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor do atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) do DSA que é identificado pela propriedade **DsaDN** .

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o caminho X. 500 do NC (contexto de nomenclatura) que está associado a esta operação.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) do NC que é identificado pela propriedade **NamingContextDN** .

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a hora em que a operação foi iniciada. **NULL** se essa operação ainda estiver na fila.

</dd> <dt>

**Opções**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o conjunto de sinalizadores que fornece dados adicionais sobre a operação. O conteúdo desse membro é determinado pelo valor da propriedade **OpType** .

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronização de \_ tipo de op DS repl \_ \_**


</dt> <dd>

Contém zero ou uma combinação de um ou mais dos **DS \_ \_ \* REPSYNC* _ valores, conforme definido para o parâmetro _Options * em [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ \_ Adicionar tipo de op \_ do DS repl**


</dt> <dd>

Contém zero ou uma combinação de um ou mais dos **DS \_ \_ \* REPADD* _ valores, conforme definido para o parâmetro _Options * em [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_exclusão do \_ tipo de op DS repl \_ \_**


</dt> <dd>

Contém zero ou uma combinação de um ou mais dos **DS \_ \_ \* REPDEL* _ valores, conforme definido para o parâmetro _Options * em [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_modificação de \_ tipo de op \_ \_ do DS repl**


</dt> <dd>

Contém zero ou uma combinação de um ou mais dos **DS \_ \_ \* REPMOD* _ valores, conforme definido para o parâmetro _Options * em [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_referências de \_ atualização do tipo de op DS repl \_ \_ \_**


</dt> <dd>

Contém zero ou uma combinação de um ou mais dos **DS \_ \_ \* REPSUPD* _ valores, conforme definido para o parâmetro _Options * em [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor do [**\_ tipo de \_ op \_ DS repl**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) que indica o tipo de operação que essa classe representa.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a posição desta operação na fila.

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a prioridade desta operação. As tarefas de prioridade mais alta são executadas primeiro. A prioridade é calculada pelo servidor com base no tipo de operação que essa classe representa e nos parâmetros da operação.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém a ID da operação, que é exclusiva por máquina e por inicialização.

</dd> <dt>

**Enfileirado**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a hora em que essa operação foi adicionada à fila.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

