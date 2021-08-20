---
description: O método GetNextSrc2 pesquisa a faixa para a próxima fonte que aparece na hora especificada ou posterior. Esse método é equivalente a IAMTimelineTrack::GetNextSrc, mas obtém um valor REFTIME.
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: Método IAMTimelineTrack::GetNextSrc2 (Qedit.h)
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
ms.openlocfilehash: ca9b18ba6ddd56771ac738f0ff831e4ea284d995fb28582a578386321e7ef856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154817"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Método IAMTimelineTrack::GetNextSrc2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextSrc2` método pesquisa a faixa para a próxima origem que aparece na hora especificada ou posterior. Esse método é equivalente a [**IAMTimelineTrack::GetNextSrc,**](iamtimelinetrack-getnextsrc.md)mas obtém um [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
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

Na entrada, contém a hora de início da pesquisa, em segundos. Se o método recuperar uma origem, ele define o valor para a hora de parada da origem. Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o método recuperar uma origem ou S FALSE caso \_ contrário.

## <a name="remarks"></a>Comentários

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

 

 




