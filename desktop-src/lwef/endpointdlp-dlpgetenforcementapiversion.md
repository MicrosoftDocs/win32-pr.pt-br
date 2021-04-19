---
description: Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.
title: Função DlpGetEnforcementApiVersion (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495360"
---
# <a name="dlpgetenforcementapiversion-function"></a>Função DlpGetEnforcementApiVersion

Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MajorVersion* \[ no\]
</dt> <dd>

Um **DWORD** especificando o número de versão principal.

</dd> </dl>

<dl> <dt>

*MajorVersion* \[ no\]
</dt> <dd>

Um **DWORD** especificando o número de versão secundária.

</dd> </dl>


## <a name="return-value"></a>Retornar valor

Retorna um HRESULT que inclui, mas não se limita a, os valores a seguir.

| HRESULT | Descrição |
|---------|-------------|
| S_OK | A função foi concluída com êxito |




## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |