---
description: A propriedade AnglesAvailable recupera o número de ângulos disponíveis no momento.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propriedade AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749645"
---
# <a name="anglesavailable-property"></a>Propriedade AnglesAvailable

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `AnglesAvailable` propriedade recupera o número de ângulos disponíveis no momento.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro de 1 a 9 que representa o número de ângulos disponíveis no momento. If


```
iAngles
```



= 1, não há nenhum bloco de ângulo no local atual.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. Um *bloco de ângulo* é um segmento de vídeo que foi capturado de mais de um ângulo de câmera. Pode haver até nove ângulos em um bloco de ângulo, numerados de 1 a 9. Quando o navegador de DVD entra primeiro em um bloco de ângulo, ele envia ao aplicativo uma \_ notificação de evento de ângulos de DVD EC \_ \_ disponíveis com o número de ângulos em *lParam1*. Um disco pode ser criado para mostrar automaticamente um menu para os ângulos disponíveis quando ele entra em um bloco de ângulo, mas geralmente um aplicativo deve determinar o número de ângulos disponíveis e oferecer ao usuário uma maneira de selecionar um.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



