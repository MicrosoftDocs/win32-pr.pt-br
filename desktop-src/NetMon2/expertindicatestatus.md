---
description: A função ExpertIndicateStatus indica a porcentagem de conclusão da análise de especialistas do arquivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Função ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089974"
---
# <a name="expertindicatestatus-function"></a>Função ExpertIndicateStatus

A função **ExpertIndicateStatus** indica a porcentagem de conclusão da análise do especialista do arquivo de captura.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*Status* \[ do no\]
</dt> <dd>

Status atual da análise. Especifique um dos seguintes valores de [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) .



| Valor                                                                                                                                                                                 | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INativo**</dt> </dl> | O especialista nunca começou. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**EXPERTSTATUS \_ iniciando**</dt> </dl> | O especialista está sendo iniciado. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ em execução**</dt> </dl>    | O especialista está em execução normalmente. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**problema de EXPERTSTATUS \_**</dt> </dl>    | Um problema especificado no parâmetro substatus interrompeu o especialista. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ anulado**</dt> </dl>    | Monitor de Rede parou o especialista. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ concluído**</dt> </dl>             | O especialista concluiu a análise com êxito. <br/>                     |



 

</dd> <dt>

*Substatus* \[ no\]
</dt> <dd>

Extensão ou esclarecimento das informações fornecidas pelo parâmetro *status* .

</dd> <dt>

*szText* \[ no\]
</dt> <dd>

Indicador de status de texto opcional.

Esse valor de parâmetro pode ser **nulo**.

</dd> <dt>

*PercentDone* \[ fora\]
</dt> <dd>

Porcentagem dos dados de captura que o especialista processou.

Quando o especialista conclui com êxito a análise de um arquivo de captura, o sistema define o percentual como 100. Qualquer número maior que 99 será ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será NMERR \_ especialista \_ . o especialista deverá limpar e retornar imediatamente sem concluir a captura.

## <a name="remarks"></a>Comentários

A função **ExpertIndicateStatus** só pode ser chamada por especialistas que implementam a função [executar](run.md) ou [Configurar](configure.md) exportação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
