---
description: O método Put log de erros \_ especifica um registro de erro para o objeto.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'IAMSetErrorLog: método de ut_ErrorLog de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757685"
---
# <a name="iamseterrorlogput_errorlog-method"></a>Método IAMSetErrorLog::p UT log de \_ erros

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_ErrorLog` método especifica um log de erros para o objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Ponteiro para a interface [**IAMErrorLog**](iamerrorlog.md) do log de erros.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

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

 

 




