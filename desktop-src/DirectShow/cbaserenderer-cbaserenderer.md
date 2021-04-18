---
description: Método de construtor.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Construtor CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749630"
---
# <a name="cbaserenderercbaserenderer-constructor"></a>Construtor CBaseRenderer. CBaseRenderer

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificador de classe do renderizador.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Recebe um valor **HRESULT** .

</dd> <dt>

*TimerResolution* 
</dt> <dd>

Resolução do temporizador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




