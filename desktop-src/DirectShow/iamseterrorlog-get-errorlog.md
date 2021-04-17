---
description: O método Get Outlog \_ recupera o log de erros atual deste objeto.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Método IAMSetErrorLog:: get_ErrorLog (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747566"
---
# <a name="iamseterrorlogget_errorlog-method"></a>Método de log de erros IAMSetErrorLog:: get \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_ErrorLog` método recupera o log de erros atual para este objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMErrorLog**](iamerrorlog.md) do log de erros. Se a linha do tempo não tiver um log de erros, o valor será definido como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o valor retornado em *PVal* não for **NULL**, a interface [**IAMErrorLog**](iamerrorlog.md) terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMSetErrorLog**](iamseterrorlog.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




