---
description: O método put \_ Top define a coordenada da janela superior.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: CBaseControlWindow.put_Top método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3332bcf90ac5e2ee776fe7110c958e50b838bcbdbc6bb4abb23850ced12cc28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635826"
---
# <a name="cbasecontrolwindowput_top-method"></a>Método CBaseControlWindow.put \_ Top

O `put_Top` método define a coordenada da janela superior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Top* 
</dt> <dd>

Nova coordenada superior, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

A janela tem uma posição na área de trabalho. Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior). As interfaces automatizadas pelo OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; essa é a convenção usada em DirectShow. Todas as coordenadas são expressas em pixels e alterar qualquer coordenada atualizará a janela imediatamente.

Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm nenhum efeito sobre a largura e a altura da janela. Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




