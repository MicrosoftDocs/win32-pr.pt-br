---
title: Função MpManagerStatusQuery (MpClient. h)
description: Retorna informações de status sobre vários componentes do Malware Protection Manager. | Função MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Recursos do ambiente Windows herdado da função MpManagerStatusQuery
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298099"
---
# <a name="mpmanagerstatusquery-function"></a>Função MpManagerStatusQuery

\[**MpManagerStatusQuery** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]

Retorna informações de status sobre vários componentes do Malware Protection Manager.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
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

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**informações de MPSTATUS \_**](mpstatus-info.md)
</dt> </dl>

 

 





