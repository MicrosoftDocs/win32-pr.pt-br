---
description: Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Função DlpInitializeEnforcementMode (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: be1e71782b258745e31d286a69ae76d3ecbcafb74c170f3b5baf5eb19bcc4b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610436"
---
# <a name="dlpinitializeenforcementmode-function"></a>Função DlpInitializeEnforcementMode

Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Um **DWORD** especificando o número de operações incluídas na matriz *OperationEnforcement* .

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ no\]
</dt> <dd>

Uma matriz de estruturas [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) que especificam o nível de imposição para uma operação de DLP de ponto de extremidade.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retorna um HRESULT que inclui, mas não se limita a, os valores a seguir.

| HRESULT | Descrição |
|---------|-------------|
| S_OK | A função foi concluída com êxito |
| E_INVALIDARG | Um ou mais dos parâmetros de função são inválidos. |
| E_OUTOFMEMORY | Falha na alocação de memória para a operação. |



## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |