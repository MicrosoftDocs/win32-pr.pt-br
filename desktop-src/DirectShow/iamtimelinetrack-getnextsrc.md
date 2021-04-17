---
description: O método GetNextSrc pesquisa o roteiro para a próxima fonte que aparece na hora especificada ou posteriormente.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Método IAMTimelineTrack:: GetNextSrc (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766306"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>Método IAMTimelineTrack:: GetNextSrc

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextSrc` método pesquisa a próxima fonte que aparece na hora especificada ou posteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSrc* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.

</dd> <dt>

*Aquecimento* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início da pesquisa, em unidades de 100 a nanossegundos. Se o método recuperar uma origem, ele definirá o valor para a hora de parada da origem. Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-la.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o método recuperar uma origem, ou S \_ false caso contrário.

## <a name="remarks"></a>Comentários

Se o tempo especificado por *pinagem* estiver entre as horas de início e de parada de uma origem, o método recuperará essa fonte.

Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




