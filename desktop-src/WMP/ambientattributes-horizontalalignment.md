---
title: AmbientAttributes.horizontalAlignment
description: O atributo horizontalAlignment especifica ou recupera um valor que indica o posicionamento horizontal do controle quando VIEW ou SUBVIEW pai é ressalvado.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbienteAttributes.horizontalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf64189735d79e1ad3eb4f7b3637ca68cfdae489cda9423bb60acdd1f9185c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055164"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes.horizontalAlignment

O **atributo horizontalAlignment** especifica ou recupera um valor que indica o posicionamento horizontal do controle quando **VIEW** ou **SUBVIEW** pai é ressalvado.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**



| Valor   | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| esquerda    | Padrão. Mantém o posicionamento do controle em relação à esquerda do **VIEW** ou **SUBVIEW** pai quando a exibição é ressada.                                                                                                                                                                                                                               |
| direita   | Mantém o posicionamento do controle em relação à direita do **VIEW** ou **SUBVIEW** pai quando a exibição é ressada.                                                                                                                                                                                                                                       |
| centro  | Mantém o posicionamento do controle em relação ao centro horizontal do **VIEW** ou **SUBVIEW** pai quando a exibição é relizada.                                                                                                                                                                                                                           |
| Esticar | Mantém o posicionamento do controle em relação às margens esquerda e direita do **VIEW** ou **SUBVIEW** pai quando reessado. O controle se alonga para ajustar quando **VIEW** ou **SUBVIEW** é alongado. A imagem real não aumenta ou diminui, a menos que seja reizável, mas a área clicável aumenta ou diminui se não estiver limitada por um **recorteImagem**. |



 

## <a name="remarks"></a>Comentários

A menos **que horizontalAlignment** esteja definido como "center", o controle manterá sua distância original da borda especificada ou das duas bordas se "stretch" for especificado e o controle for resizável. Se o controle não for resizável e "stretch" for especificado, a região clicável será alongada.

Você pode definir qualquer combinação de **horizontalAlignment** e **verticalAlignment**. Por exemplo, se você quiser centralizar um controle horizontal e verticalmente, de definido horizontalAlignment="center" verticalAlignment="center".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





