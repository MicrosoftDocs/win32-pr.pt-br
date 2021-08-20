---
title: Classificações
description: Classificações
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player Aparências móveis, classificações
- capas, classificações
- referência para capas, classificações
- classificações em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eec9b28ef77c59b4ca2303c96426009f34b817c65e853071febc76507c3aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934069"
---
# <a name="ratings"></a>Classificações

ao criar uma capa para Windows Media Player 10,1 Mobile, você pode exibir a classificação associada ao conteúdo com base em áudio Windows Media que está sendo reproduzido no momento. A classificação é exibida como uma estrela com um número. A estrela será numerada uma a cinco, denotando a classificação atual desse conteúdo. Se o conteúdo não for classificado, a estrela será numerada como zero.

A seção ratings do arquivo de definição de capa começa com esta linha:


```C++
[ Ratings ]

```



Em seguida, você deve adicionar uma linha que contém informações sobre o tamanho e o local do ícone de classificações em sua capa.


```C++
147, 3, 22, 21       ratings96S.gif

```



Você pode usar o modelo a seguir para a seção de classificações do arquivo de definição de capa:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



você também pode atribuir um valor de classificações a um item de mídia por meio da interface do usuário no Windows Media Player 10,1 Mobile e, na próxima vez que o dispositivo for sincronizado com o computador, o novo valor de classificações será propagado para esse item de mídia se ele residir na biblioteca do Windows Media Player 10.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




