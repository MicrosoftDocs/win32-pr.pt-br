---
title: Função MpManagerVersionQuery (MpClient. h)
description: Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Recursos do ambiente Windows herdado da função MpManagerVersionQuery
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
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758144"
---
# <a name="mpmanagerversionquery-function"></a>Função MpManagerVersionQuery

Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*pVersionInfo* \[ fora\]
</dt> <dd>

Tipo: **\_ informações de PMPVERSION**

Ponteiro para uma estrutura que contém informações de versão sobre vários componentes do Malware Protection Manager. Consulte [**MPVERSION \_ info**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

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

[**informações de MPVERSION \_**](mpversion-info.md)
</dt> </dl>

 

 





