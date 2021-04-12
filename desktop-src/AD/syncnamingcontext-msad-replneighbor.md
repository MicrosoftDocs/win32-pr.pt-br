---
title: Método SyncNamingContext da classe MSAD_ReplNeighbor
description: Chama a função DsReplicaSync que sincroniza um contexto de nomenclatura de destino com uma de suas origens.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory do método SyncNamingContext
- Método SyncNamingContext Active Directory, classe MSAD_ReplNeighbor
- Classe MSAD_ReplNeighbor Active Directory, método SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455669"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Método SyncNamingContext da \_ classe REPLNEIGHBOR MSAD

Chama a função [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) que sincroniza um contexto de nomenclatura de destino com uma de suas origens.

## <a name="syntax"></a>Sintaxe


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Opções* \[ do no\]
</dt> <dd>

Dados adicionais que determinam como o método processa a solicitação. Esse parâmetro pode ser uma combinação dos valores a seguir.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Adicionar referência de REPSYNC DS \_**


</dt> <dd>

Faz com que o DSA (Directory System Agent de origem) Verifique se o DSA local está presente na lista replicações de origem para. Se o DSA local não estiver presente, ele será adicionado. Isso garante que a origem envie notificações de alteração.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ todas as \_ fontes**


</dt> <dd>

Não há suporte para esse valor.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Sincroniza de todas as fontes.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operação assíncrona de REPSYNC DS \_**


</dt> <dd>

Executa essa operação de forma assíncrona.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Necessário ao usar **DS \_ REPSYNC \_ todas as \_ fontes**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_força de REPSYNC DS \_**


</dt> <dd>

Sincroniza mesmo que o link esteja desabilitado no momento.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ completo**


</dt> <dd>

Sincroniza a partir do primeiro número de sequência de atualização (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_sistema de \_ mensagens entre sites REPSYNC DS \_**


</dt> <dd>

Sincroniza usando um ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**\_REPSYNC DS \_ sem \_ descarte**


</dt> <dd>

Não descarta essa solicitação de sincronização, mesmo que uma sincronização semelhante esteja pendente.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ periódico**


</dt> <dd>

Indica que esta operação é uma solicitação de sincronização periódica agendada pelo administrador.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ urgente**


</dt> <dd>

Indica que esta operação é uma notificação de uma atualização que está marcada como urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ gravável**


</dt> <dd>

Indica que esta réplica é gravável. Se esse sinalizador não for definido, a réplica será somente leitura.

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

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





