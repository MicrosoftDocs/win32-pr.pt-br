---
title: Função MpManagerVersionQuery (MpClient.h)
description: Retorna informações de versão sobre vários componentes do gerenciador de proteção contra malware.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Função MpManagerVersionQuery herdado Windows ambiente
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6407f36650b699f6bcdc9cbdd832ff2db38f68e9db758411d42aa5e81564ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114536"
---
# <a name="mpmanagerversionquery-function"></a>Função MpManagerVersionQuery

Retorna informações de versão sobre vários componentes do gerenciador de proteção contra malware.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ Em\]
</dt> <dd>

Tipo: **MPHANDLE**

Lidar com a interface do gerenciador de proteção contra malware. Esse handle é retornado pela [**função MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*pVersionInfo* \[ out\]
</dt> <dd>

Tipo: **PMPVERSION \_ INFO**

Ponteiro para uma estrutura que contém informações de versão sobre vários componentes do gerenciador de proteção contra malware. Consulte [**INFORMAÇÕES \_ DO MPVERSION.**](mpversion-info.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem-sucedida, o valor de retorno **será S \_ OK.**

Se a função falhar, o valor de retorno será um código **HRESULT com** falha. O chamador pode usar a [**função MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO MPVERSION**](mpversion-info.md)
</dt> </dl>

 

 





