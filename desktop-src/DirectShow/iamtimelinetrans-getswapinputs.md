---
description: O método GetSwapInputs recupera um valor que indica se as entradas de transição são trocadas.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Método IAMTimelineTrans:: GetSwapInputs (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 566dbc54b30619c67ffb9d804e4854d51cae86d3688bda0b48eebfeb64cdb749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316296"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>Método IAMTimelineTrans:: GetSwapInputs

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSwapInputs` método recupera um valor que indica se as entradas de transição são trocadas.

Por padrão, uma transição é proveniente da composição de todas as camadas de prioridade inferior para a camada em que reside a transição. Você pode reverter essa progressão, de modo que a transição vai da camada onde ela reside de volta para a composição de camadas de prioridade inferior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe um valor booliano. Se o valor for **false**, a transição passará da composição de todas as camadas de prioridade inferior para a camada de transição. Se o valor for **true**, a transição irá para a direção oposta. O valor padrão é **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




