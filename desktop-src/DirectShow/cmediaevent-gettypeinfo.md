---
description: Método CMediaEvent. GetTypeInfo – recupera um objeto Type-Information, que pode recuperar as informações de tipo de uma interface.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f93e3227051729f9d16e1f9ef8de464a14cca33b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095564"
---
# <a name="cmediaeventgettypeinfo-method"></a>Método CMediaEvent. GetTypeInfo

Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*itinfo* 
</dt> <dd>

Digite as informações a serem retornadas. Passe zero para recuperar informações de tipo para a implementação de **IDispatch** .

</dd> <dt>

*lcid* 
</dt> <dd>

ID de localidade para as informações de tipo. Para classes que dão suporte a nomes de membros localizados, um objeto poderá retornar informações de tipo diferentes para idiomas diferentes. Para classes que não dão suporte a nomes de membros localizados, esse parâmetro pode ser ignorado.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Endereço de um ponteiro para o objeto Type-informations solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um \_ ponteiro E se *ppTInfo* for inválido. Retorna o tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* não for zero. Retornará S \_ OK se for bem-sucedido. Caso contrário, retorna um **HRESULT** de uma das chamadas para recuperar o tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




