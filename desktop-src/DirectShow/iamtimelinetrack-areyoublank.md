---
description: O método AreYouBlank determina se a faixa está em branco (não contém nenhum objeto de origem).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'Método IAMTimelineTrack:: AreYouBlank (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779848"
---
# <a name="iamtimelinetrackareyoublank-method"></a>Método IAMTimelineTrack:: AreYouBlank

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `AreYouBlank` método determina se a faixa está em branco (não contém nenhum objeto de origem).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe um valor booliano que especifica se a faixa está em branco. Se o valor for **true**, a faixa ficará em branco e não conterá nenhum objeto de origem. Se for **false**, a faixa não ficará em branco.

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

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




