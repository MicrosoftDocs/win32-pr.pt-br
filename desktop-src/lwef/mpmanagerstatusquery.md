---
title: Função MpManagerStatusQuery (MpClient. h)
description: Retorna informações de status sobre vários componentes do Malware Protection Manager. | Função MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- recursos de ambiente de Windows herdado da função MpManagerStatusQuery
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
ms.openlocfilehash: 9d05751f30e1579ef8b12e31a4f858469b1c997cf9c29d7643c0600a133840fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883371"
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

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**. Essa chamada de função tem garantia de sucesso mesmo que um serviço Antimalware não esteja em execução.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
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

 

 





