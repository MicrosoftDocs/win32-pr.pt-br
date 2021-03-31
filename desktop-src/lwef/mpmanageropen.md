---
title: Função MpManagerOpen (MpClient. h)
description: Estabelece uma conexão com o Malware Protection Manager no computador local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Recursos do ambiente Windows herdado da função MpManagerOpen
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
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645070"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





