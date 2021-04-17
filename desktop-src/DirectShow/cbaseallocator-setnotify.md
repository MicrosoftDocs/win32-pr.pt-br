---
description: 'O método setnotificate define ou remove um retorno de chamada no alocador. O alocador chama o método de retorno de chamada sempre que o método IMemAllocator:: ReleaseBuffer do alocador é chamado.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Método CBaseAllocator. setnotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756000"
---
# <a name="cbaseallocatorsetnotify-method"></a>Método CBaseAllocator. setnotificar

\[[**Setnotificar**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) pode ser alterado ou indisponível nas versões subsequentes.\]

O `SetNotify` método define ou remove um retorno de chamada no alocador. O alocador chama o método de retorno de chamada sempre que o método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) do alocador é chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNotify* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) que será usada para o retorno de chamada. O chamador deve implementar a interface. Use o valor **NULL** para remover o retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método implementa o método [**IMemAllocatorCallbackTemp:: Setnotificar**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) . O alocador não expõe a interface [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , a menos que o sinalizador *fEnableReleaseCallback* seja definido como **true** no construtor [**CBaseAllocator**](cbaseallocator.md) .

Esse método define a variável de membro [**CBaseAllocator:: m \_ pNotify**](cbaseallocator-m-pnotify.md) igual a *pNotify* e incrementa a contagem de referência na interface. Se *m \_ pNotify* for não **nulo**, o método **ReleaseBuffer** do alocador chamará [**IMemAllocatorNotifyCallbackTemp:: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease). Consulte a seção comentários nesse método para obter informações sobre como implementar o retorno de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




