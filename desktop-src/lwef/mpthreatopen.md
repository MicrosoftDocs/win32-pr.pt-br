---
title: Função MpThreatOpen (MpClient. h)
description: Retorna um identificador de enumeração para a finalidade de recuperar ameaças.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- recursos de ambiente de Windows herdado da função MpThreatOpen
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949fd1c8291ecb183cf51cf5385fe356a33cb1288978fda42f37d748f1a162a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746885"
---
# <a name="mpthreatopen-function"></a>Função MpThreatOpen

Retorna um identificador de enumeração para a finalidade de recuperar ameaças. Essa função pode ser usada para abrir ameaças detectadas por uma verificação específica, todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou todas as ameaças presentes no banco de dados de assinatura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hScanHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Pode ser um identificador para uma operação de verificação concluída, retornada pela função [**MpScanStart**](mpscanstart.md) . Como alternativa, esse parâmetro pode ser definido como o identificador de interface do Malware Protection Manager retornado por [**MpManagerOpen**](mpmanageropen.md) para enumerar todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou ameaças do banco de dados de assinatura.

</dd> <dt>

*Ameaçador* \[ no\]
</dt> <dd>

Tipo: **\_ origem do MPTHREAT**

Usado para controlar a origem da enumeração de ameaças. Os valores possíveis para esse parâmetro são:



| Valor                                                                                                                                                                                                 | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**\_verificação de origem do MPTHREAT \_**</dt> </dl>                   | Ameaças associadas ao identificador de verificação específico.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**\_origem MPTHREAT \_ ativa**</dt> </dl>             | Ameaças atualmente ativas no sistema.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**MPTHREAT \_ histórico de origem \_**</dt> </dl>          | Ameaças que são acionadas e preservadas como um histórico.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**\_quarentena de origem do MPTHREAT \_**</dt> </dl> | Ameaças que estão em quarentena.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**\_assinatura de origem do MPTHREAT \_**</dt> </dl>    | Ameaças que são possíveis detectar com o banco de dados de assinatura atual.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**\_estado de origem do MPTHREAT \_**</dt> </dl>                | Ameaças que foram acionadas recentemente. ("Recentemente" é definido por uma configuração interna configurável.)<br/> |



 

</dd> <dt>

*Threattype* \[ no\]
</dt> <dd>

Tipo: **\_ tipo de MPTHREAT**

Usado para filtrar ameaças enumeradas com base no tipo de detecção. Os valores possíveis para esse parâmetro são:



| Valor                                                                                                                                                                                           | Significado                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT \_ tipo \_ KNOWNBAD**</dt> </dl>       | A detecção é executada com base em uma assinatura, emulação ou outro método de detecção de ameaças específico.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**tipo de MPTHREAT \_ \_ suspeito**</dt> </dl> | A detecção é executada com base no monitoramento de comportamento.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**tipo de MPTHREAT \_ \_ desconhecido**</dt> </dl>          | A detecção é executada com base em ameaças desconhecidas (não classificadas).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT \_ tipo \_ KNOWNGOOD**</dt> </dl>    | A detecção é realizada com base em ameaças seguras conhecidas.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ tipo \_ NIS**</dt> </dl>                      | A detecção é realizada com base em ameaças NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ fora\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de enumeração de ameaça retornado que identifica o contexto de enumeração. Esse identificador pode ser usado para enumerar informações de ameaças usando o [**MpThreatEnumerate**](mpthreatenumerate.md). O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





