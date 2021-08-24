---
title: Função MpManagerStatusQueryEx (MpClient.h)
description: Retorna informações de status sobre vários componentes do gerenciador de proteção contra malware. | Função MpManagerStatusQueryEx (MpClient.h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Função MpManagerStatusQueryEx herdou Windows ambiente
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8d7e3e6135a5f01691528480b760cfea422c78b9c032219f6e100da5ebd929d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961106"
---
# <a name="mpmanagerstatusqueryex-function"></a>Função MpManagerStatusQueryEx

Retorna informações de status sobre vários componentes do gerenciador de proteção contra malware.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ Em\]
</dt> <dd>

Tipo: **MPHANDLE**

Lidar com a interface do gerenciador de proteção contra malware. Esse handle é retornado pela [**função MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*dwFlag* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Controla quais informações de consulta são retornadas. Algumas informações são caras e podem não ser necessárias.



| Valor                                                                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAGS \_ NONE**</dt> </dl>       | Padrão.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**SINALIZADOR DE CONSULTA DE STATUS DO MP \_ \_ \_ \_ NOSTATE**</dt> </dl> | Não consulte informações de estado.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Tipo: **PMPSTATUS \_ INFO**

Ponteiro para uma estrutura que retorna informações de status sobre as últimas verificações, ameaças ativas e vários status de componente. Consulte [**INFORMAÇÕES \_ DO MPSTATUS.**](mpstatus-info.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem-sucedida, o valor de retorno **será S \_ OK.** Essa chamada de função terá êxito mesmo se um serviço AntiMalware não estiver em execução.

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

[**INFORMAÇÕES DE \_ MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





