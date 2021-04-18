---
description: 'O método GetTransAtTime2 recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas. Esse método é equivalente a IAMTimelineTransable:: GetTransAtTime, mas usa um parâmetro REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Método IAMTimelineTransable:: GetTransAtTime2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760085"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>Método IAMTimelineTransable:: GetTransAtTime2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetTransAtTime2` método recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas. Esse método é equivalente a [**IAMTimelineTransable:: GetTransAtTime**](iamtimelinetransable-gettransattime.md), mas usa um parâmetro [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppObj* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição.

</dd> <dt>

*Hora* 
</dt> <dd>

Hora a partir da qual iniciar a pesquisa, em segundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                  | Descrição                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>      | Nenhuma transição foi encontrada.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | A transição foi encontrada.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/>          |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/> |



 

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




