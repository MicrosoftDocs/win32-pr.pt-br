---
title: Método ExecuteKCC da classe MSAD_DomainController classe
description: Chama a função DsReplicaConsistencyCheck, que invoca o KCC (Knowledge Consistency Checker) para verificar a topologia de replicação.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Método ExecuteKCC Active Directory
- Método ExecuteKCC Active Directory , MSAD_DomainController classe
- MSAD_DomainController classe active directory , método ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48295638f105b79ea24a55965ca3ec75ee0ad6b9982c74664f8bfecdd0681cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189609"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Método ExecuteKCC da classe DomainController do MSAD \_

Chama a [**função DsReplicaConsistencyCheck,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) que invoca o KCC (Knowledge Consistency Checker) para verificar a topologia de replicação.

## <a name="syntax"></a>Sintaxe


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TaskID* \[ Em\]
</dt> <dd>

A tarefa que o KCC deve executar. **DS \_ KCC \_ TASKID \_ UPDATE \_ TOPOLOGY** é o único valor com suporte no momento.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um conjunto de sinalizadores que modificam o comportamento do **método ExecuteKCC.** Esse parâmetro pode ser zero ou uma combinação de um ou mais dos valores a seguir.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**OPERAÇÃO \_ \_ ASSÍNCRONA DO SINALIZADOR DE KCC \_ \_ DS**


</dt> <dd>

A tarefa é enxadada e, em seguida, a função retorna sem aguardar a conclusão da tarefa.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**SINALIZADOR \_ KCC DS \_ \_ SEM SINAL**


</dt> <dd>

A tarefa não será adicionada à fila se outra tarefa na fila for executado em breve.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DomainController do MSAD \_**](msad-domaincontroller.md)
</dt> </dl>

 

 





