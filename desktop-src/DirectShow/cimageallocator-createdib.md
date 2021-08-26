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
ms.openlocfilehash: 94a629831ea50219b47500c0637cfeaebfbc95b1ee99a8b9d3872a655ab5485c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055476"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




