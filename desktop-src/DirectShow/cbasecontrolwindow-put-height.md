---
description: O método put \_ Height define a altura da janela.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: CBaseControlWindow.put_Height método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34774d366858e9c9bbe9ce5b02e897453bca21b9bd07d9eb11c60ac8313d33e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660033"
---
# <a name="cbasecontrolwindowput_height-method"></a>Método Height CBaseControlWindow.put \_

O `put_Height` método define a altura da janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Altura* 
</dt> <dd>

Nova altura da janela, em pixels.

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

 

 




