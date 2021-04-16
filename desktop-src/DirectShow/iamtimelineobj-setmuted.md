---
description: O método com mudo definido define o estado mudo do objeto. Um objeto sem áudio não é renderizado, mas permanece na linha do tempo.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Método IAMTimelineObj:: setmudoed (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758680"
---
# <a name="iamtimelineobjsetmuted-method"></a>Método IAMTimelineObj:: setmudoed

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMuted` método define o estado mudo do objeto. Um objeto sem áudio não é renderizado, mas permanece na linha do tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* 
</dt> <dd>

Sinalizador que especifica o estado mudo. Se **for true**, o objeto e todos os seus filhos ficarão sem áudio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Mudo de um objeto também desativa todos os filhos contidos no objeto. Por exemplo, se você ativar mudo de uma faixa, as transições, as fontes e os efeitos nessa faixa também ficarão sem áudio. Depois que o objeto não estiver mais mudo, seus filhos serão revertidos para seu estado anterior, o que pode estar mudo ou sem áudio.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




