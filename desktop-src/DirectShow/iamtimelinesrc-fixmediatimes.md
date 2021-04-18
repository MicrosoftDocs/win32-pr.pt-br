---
description: O método FixMediaTimes arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Em geral, os aplicativos não precisam chamar esse método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Método IAMTimelineSrc:: FixMediaTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758059"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>Método IAMTimelineSrc:: FixMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `FixMediaTimes` método arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Em geral, os aplicativos não precisam chamar esse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em unidades de 100 a nanossegundos. Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em unidades de 100 a nanossegundos. Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é semelhante ao método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , mas preserva a proporção original de tempos de mídia e tempos de linha do tempo. Apenas arredondar os horários para o limite de quadro mais próximo poderia distorcer essa proporção.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




