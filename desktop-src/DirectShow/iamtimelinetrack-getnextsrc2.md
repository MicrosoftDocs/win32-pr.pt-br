---
description: 'O método GetNextSrc2 pesquisa o roteiro para a próxima fonte que aparece na hora especificada ou posteriormente. Esse método é equivalente a IAMTimelineTrack:: GetNextSrc, mas usa um valor de REFTIME.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Método IAMTimelineTrack:: GetNextSrc2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784022"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Método IAMTimelineTrack:: GetNextSrc2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextSrc2` método pesquisa a próxima fonte que aparece na hora especificada ou posteriormente. Esse método é equivalente a [**IAMTimelineTrack:: GetNextSrc**](iamtimelinetrack-getnextsrc.md), mas usa um valor de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
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

Na entrada, contém a hora de início da pesquisa, em segundos. Se o método recuperar uma origem, ele definirá o valor para a hora de parada da origem. Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-la.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o método recuperar uma origem, ou S \_ false caso contrário.

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

 

 




