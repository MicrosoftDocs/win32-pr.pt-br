---
description: Construtor de CBaseVideoRenderer. CBaseVideoRenderer-método de construtor.
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
ms.openlocfilehash: ec6a5e12d12b12f22cf1089d85ed4c07656da86cda071d8645355890996e2cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954755"
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
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




