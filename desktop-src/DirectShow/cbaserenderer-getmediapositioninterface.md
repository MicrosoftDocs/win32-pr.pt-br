---
description: O método GetMediaPositionInterface recupera os ponteiros de interface IMediaPosition e IMediaSeeking do filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Método CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811749"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Método CBaseRenderer. GetMediaPositionInterface

O `GetMediaPositionInterface` método recupera os ponteiros de interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de referência da interface.

</dd> <dt>

*ppv* 
</dt> <dd>

Endereço de uma variável que recebe o ponteiro de interface.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>     |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Interface sem suporte.<br/> |



 

## <a name="remarks"></a>Comentários

O filtro Delega todos os comandos de busca a um objeto [**CRendererPosPassThru**](crendererpospassthru.md) , que passa por upstream. Esse método criará o objeto **CRendererPosPassThru** , se ele ainda não existir, e o consultará para a interface solicitada.

A variável de membro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) armazena um ponteiro para o objeto **CRendererPosPassThru** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




