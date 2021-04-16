---
title: Função MpManagerStatusQueryEx (MpClient. h)
description: Retorna informações de status sobre vários componentes do Malware Protection Manager. | Função MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Recursos do ambiente Windows herdado da função MpManagerStatusQueryEx
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
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105758146"
---
# <a name="mpmanagerstatusqueryex-function"></a>Função MpManagerStatusQueryEx

Retorna informações de status sobre vários componentes do Malware Protection Manager.

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

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwFlag* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Controla quais informações de consulta são retornadas. Algumas informações são caras e podem não ser necessárias.



| Valor                                                                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**sinalizadores de consulta de status do MP \_ \_ \_ \_ nenhum**</dt> </dl>       | Padrão.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**sinalizador de consulta de status do MP \_ \_ \_ \_ nostate**</dt> </dl> | Não consulte informações de estado.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ fora\]
</dt> <dd>

Tipo: **\_ informações de PMPSTATUS**

Ponteiro para uma estrutura que retorna informações de status sobre as últimas verificações, ameaças ativas e vários status de componente. Consulte [**MPSTATUS \_ info**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**. Essa chamada de função tem garantia de sucesso mesmo que um serviço Antimalware não esteja em execução.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**informações de MPSTATUS \_**](mpstatus-info.md)
</dt> </dl>

 

 





