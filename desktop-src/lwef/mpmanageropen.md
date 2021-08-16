---
title: Função MpManagerOpen (MpClient. h)
description: Estabelece uma conexão com o Malware Protection Manager no computador local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- recursos de ambiente de Windows herdado da função MpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324d013c46777ac48af32e6c91f557b7feda3a03fbdf0c21a7c79e8cf5e3d9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883361"
---
# <a name="mpmanageropen-function"></a>Função MpManagerOpen

Estabelece uma conexão com o Malware Protection Manager no computador local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwReserved* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Reservado para uso futuro. Deve ser definido como 0.

</dd> <dt>

*phMpHandle* \[ fora\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .

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

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





