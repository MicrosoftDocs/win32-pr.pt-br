---
description: A função ExpertIndicateStatus indica o percentual de conclusão da análise de especialistas do arquivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Função ExpertIndicateStatus (Netmon.h)
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
ms.openlocfilehash: f9f40e339b450496ec4b0aff1f3e951c4d7468fa22f7b2ff3dd2f84de6b92354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012264"
---
# <a name="expertindicatestatus-function"></a>Função ExpertIndicateStatus

A **função ExpertIndicateStatus** indica o percentual de conclusão da análise do especialista do arquivo de captura.

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

*hExpertKey* \[ Em\]
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista quando ele chama a [função](run.md) Executar.

</dd> <dt>

*Status* \[ Em\]
</dt> <dd>

Status atual da análise. Especifique um dos seguintes [valores EXPERTSTATUSENUMERATION.](expertstatusenumeration.md)



| Valor                                                                                                                                                                                 | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INACTIVE**</dt> </dl> | O especialista nunca começou. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**EXPERTSTATUS \_ STARTING**</dt> </dl> | O especialista está começando. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ EM EXECUÇÃO**</dt> </dl>    | O especialista está em execução normalmente. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**PROBLEMA DE \_ EXPERTSTATUS**</dt> </dl>    | Um problema especificado no parâmetro SubStatus interrompeu o especialista. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ ABORTED**</dt> </dl>    | Monitor de Rede interrompeu o especialista. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ DONE**</dt> </dl>             | O especialista concluiu a análise com êxito. <br/>                     |



 

</dd> <dt>

*SubStatus* \[ Em\]
</dt> <dd>

Extensão ou esclarecimento das informações fornecidas pelo *parâmetro Status.*

</dd> <dt>

*sztext* \[ Em\]
</dt> <dd>

Indicador de status de texto opcional.

Esse valor de parâmetro pode ser **NULL.**

</dd> <dt>

*PercentDone* \[ out\]
</dt> <dd>

Percentual dos dados de captura que o especialista processou.

Quando o especialista conclui com êxito a análise de um arquivo de captura, o sistema define o percentual como 100. Qualquer número maior que 99 será ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será NMERR EXPERT TERMINATE; o especialista deverá limpar e retornar imediatamente sem \_ \_ concluir a captura.

## <a name="remarks"></a>Comentários

A **função ExpertIndicateStatus** só pode ser chamada por especialistas que implementam a [função Executar](run.md) ou [Configurar](configure.md) exportação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
