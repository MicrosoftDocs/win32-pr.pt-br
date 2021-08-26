---
description: O método GetNextSrc pesquisa a faixa para a próxima origem que aparece na hora especificada ou posterior.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: Método IAMTimelineTrack::GetNextSrc (Qedit.h)
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
ms.openlocfilehash: dd0257fa614a6581cc31f5416e6f1c2395fcb9444721d3668c9f2d2498e52088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904636"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>Método IAMTimelineTrack::GetNextSrc

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextSrc` método pesquisa a faixa para a próxima origem que aparece na hora especificada ou posterior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.

</dd> <dt>

*Pinagem* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início da pesquisa, em unidades de 100 nanossegundos. Se o método recuperar uma origem, ele define o valor para a hora de parada da origem. Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o método recuperar uma origem ou S FALSE caso \_ contrário.

## <a name="remarks"></a>Comentários

Se o tempo especificado por *pInOut* estiver entre os horários de início e de parada de uma origem, o método recuperará essa origem.

Se o método retornar S \_ OK, a interface **IAMTimelineObj** retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineTrack Interface**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




