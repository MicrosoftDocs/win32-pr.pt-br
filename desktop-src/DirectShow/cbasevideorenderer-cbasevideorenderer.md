---
description: Método de construtor.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Construtor CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778512"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Construtor CBaseVideoRenderer. CBaseVideoRenderer

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificador de classe para este renderizador.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma descrição usada para fins de depuração.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o objeto do proprietário agregado.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




