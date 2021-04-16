---
title: Método ExecuteKCC da classe MSAD_DomainController
description: Chama a função DsReplicaConsistencyCheck, que invoca a Knowledge Consistency Checker (KCC) para verificar a topologia de replicação.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory do método ExecuteKCC
- Método ExecuteKCC Active Directory, classe MSAD_DomainController
- Classe MSAD_DomainController Active Directory, método ExecuteKCC
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
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753875"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Método ExecuteKCC da \_ classe DOMAINCONTROLLER MSAD

Chama a função [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , que invoca a Knowledge CONSISTENCY Checker (KCC) para verificar a topologia de replicação.

## <a name="syntax"></a>Sintaxe


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TaskId* \[ no\]
</dt> <dd>

A tarefa que o KCC deve executar. **DS \_ A \_ topologia de \_ atualização \_ de TaskId do KCC** é o único valor com suporte no momento.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um conjunto de sinalizadores que modificam o comportamento do método **ExecuteKCC** . Esse parâmetro pode ser zero ou uma combinação de um ou mais dos valores a seguir.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**\_ \_ \_ operação assíncrona de sinalizador do KCC do DS \_**


</dt> <dd>

A tarefa é enfileirada e, em seguida, a função retorna sem aguardar a conclusão da tarefa.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**sinalizador do KCC do DS \_ \_ \_ úmido**


</dt> <dd>

A tarefa não será adicionada à fila se outra tarefa em fila for executada em breve.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





