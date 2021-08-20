---
description: Mapas uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiros, que podem ser usados em chamadas subsequentes para a função membro CMediaEvent::Invoke.
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent.GetIDsOfNames (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a638861bc6a01a615355f0fad05cddc00f31d3e659fc60c0be0246eb108583f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401869"
---
# <a name="cmediaeventgetidsofnames-method"></a>Método CMediaEvent.GetIDsOfNames

Mapas uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiros, que podem ser usados em chamadas subsequentes para a função membro [**CMediaEvent::Invoke.**](cmediaevent-invoke.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de referência. Reservado para uso futuro. Deve ser **NULL.**

</dd> <dt>

*rgszNames* 
</dt> <dd>

Endereço de um ponteiro para uma matriz de nomes passada a ser mapeada.

</dd> <dt>

*Cnames* 
</dt> <dd>

Contagem dos nomes a serem mapeados.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de localidade no qual interpretar os nomes.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Ponteiro para uma matriz alocada pelo chamador, cada elemento do qual contém uma ID correspondente a um dos nomes passados na *matriz rgszNames.* O primeiro elemento representa o nome do membro; os elementos subsequentes representam cada um dos parâmetros do membro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ E \_ UNKNOWN \_ CLSID**</dt> </dl> | O CLSID não foi reconhecido.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl>    | Um ou mais nomes não eram conhecidos. Os DISPIDs retornados contêm DISPID \_ UNKNOWN para cada entrada que corresponde a um nome desconhecido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Sem memória.<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




