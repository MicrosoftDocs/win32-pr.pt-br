---
description: O método GetTransAtTime recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Método IAMTimelineTransable:: GetTransAtTime (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: db81cf9a91f34699765e89f917ec31a902ebd188dc61dd77a1b909d10b09788c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399203"
---
# <a name="iamtimelinetransablegettransattime-method"></a>Método IAMTimelineTransable:: GetTransAtTime

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetTransAtTime` método recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
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

Hora a partir da qual iniciar a pesquisa, em unidades de 100 a nanossegundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>      | Nenhuma transição foi encontrada.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | A transição foi encontrada.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/>          |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/> |



 

## <a name="remarks"></a>Comentários

Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




