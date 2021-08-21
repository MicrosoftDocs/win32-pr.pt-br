---
description: Método CMediaEvent.GetTypeInfo – recupera um objeto type-information, que pode recuperar as informações de tipo para uma interface.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: 3ef3f84cce1bad88b0f1103be3584ff350afac0fd7047b5a75a5fb473a4bedcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156984"
---
# <a name="cmediaeventgettypeinfo-method"></a>Método CMediaEvent.GetTypeInfo

Recupera um objeto de informações de tipo, que pode recuperar as informações de tipo para uma interface.

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

Digite informações a retornar. Passe zero para recuperar informações de tipo para a **implementação de IDispatch.**

</dd> <dt>

*lcid* 
</dt> <dd>

ID de localidade para as informações de tipo. Para classes que suportam nomes de membros localizados, um objeto pode ser capaz de retornar informações de tipo diferentes para idiomas diferentes. Para classes que não suportam nomes de membros localizados, esse parâmetro pode ser ignorado.

</dd> <dt>

*Pptinfo* 
</dt> <dd>

Endereço de um ponteiro para o objeto type-information solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um E \_ POINTER se *pptinfo* for inválido. Retornará TYPE \_ E \_ ELEMENTNOTFOUND se *itinfo* não for zero. Retornará S \_ OK se for bem-sucedido. Caso contrário, retornará **um HRESULT** de uma das chamadas para recuperar o tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




