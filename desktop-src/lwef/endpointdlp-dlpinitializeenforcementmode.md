---
description: Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Função DlpInitializeEnforcementMode (endpointdlp. h)
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
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495350"
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


## <a name="return-value"></a>Retornar valor

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