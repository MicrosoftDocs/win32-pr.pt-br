---
description: O método SetClipVideoRect amplia a exibição de vídeo para o subretângulo especificado.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645848"
---
# <a name="setclipvideorect-method"></a>Método SetClipVideoRect

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SetClipVideoRect` método amplia a exibição de vídeo para o subretângulo especificado.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Especifica um objeto [DVDRect](dvdrect-object.md) , que contém o retângulo de recorte.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando você define um novo retângulo de recorte, o objeto amplia essa área para caber nas dimensões de exibição gerais do aplicativo. Isso cria o efeito de zoom em uma área específica da tela. Para especificar o retângulo, crie um novo objeto [DVDRect](dvdrect-object.md) e preencha suas propriedades.

O retângulo mais comum para exibição de vídeo é 720 x 540.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



