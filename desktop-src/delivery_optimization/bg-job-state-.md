---
title: Enumeração de BG_JOB_STATE (Deliveryoptimization. h)
description: A enumeração BG_JOB_STATE define valores constantes para os diferentes Estados de um trabalho.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumeração de BG_JOB_STATE
- Enumeração de BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764259"
---
# <a name="bg_job_state-enumeration"></a>Enumeração de BG_JOB_STATE

A enumeração **BG_JOB_STATE** define valores constantes para os diferentes Estados de um trabalho.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Especifica que o trabalho está na fila e aguardando para ser executado. Se um usuário fizer logoff enquanto seu trabalho estiver transferindo, o trabalho fará a transição para o estado enfileirado.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

Não há suporte.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Especifica que o faz a transferência de dados para o trabalho.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Especifica que o trabalho está suspenso (em pausa). Para suspender um trabalho, chame o método [**método ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) . O trabalho permanece suspenso até que você chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md), [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)ou [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Especifica que ocorreu um erro não recuperável (o serviço não pode transferir o arquivo). Se o erro, como um erro de acesso negado, puder ser corrigido, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) depois que o erro for corrigido. No entanto, se o erro não puder ser corrigido, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) para cancelar o trabalho ou chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para aceitar a parte de um trabalho de download que foi transferido com êxito.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Especifica que ocorreu um erro recuperável. O tentará novamente trabalhos no estado de erro transitório com base na configuração de repetição interna. O estado do trabalho será alterado para **BG_JOB_STATE_ERROR** se o trabalho não conseguir fazer o andamento (consulte [**método ibackgroundcopyjob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Especifica que o trabalho foi processado com êxito. Você deve chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar a conclusão do trabalho e tornar os arquivos disponíveis para o cliente.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Especifica que você chamou o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que seu trabalho foi concluído com êxito.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Especifica que você chamou o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) para cancelar o trabalho (remova o trabalho da fila de transferência).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





