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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095834"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




