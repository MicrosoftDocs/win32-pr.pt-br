---
description: O método CreateDIB cria um bitmap independente de dispositivo (DIB) GDI. A DIB é alocada em um bloco mempory compartilhado, que elimina uma operação de cópia quando o filtro proprietário blits a imagem.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Método CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785367"
---
# <a name="cimageallocatorcreatedib-method"></a>Método CImageAllocator. CreateDIB

O `CreateDIB` método cria um DIB (bitmap independente de dispositivo) GDI. A DIB é alocada em um bloco mempory compartilhado, que elimina uma operação de cópia quando o filtro proprietário blits a imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Insize* 
</dt> <dd>

Tamanho do bitmap.

</dd> <dt>

*DibData* \[ referência\]
</dt> <dd>

Referência a uma estrutura [**DIBDATA**](dibdata.md) . O método preenche essa estrutura com informações sobre o DIB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




