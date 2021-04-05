---
description: O método de menu de exibição exibe o menu especificado na tela.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Método de menu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645971"
---
# <a name="showmenu-method"></a>Método de menu

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `ShowMenu` método exibe o menu especificado na tela.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Especifica a ID do menu como um inteiro.



| Valor | Descrição |
|-------|-------------|
| 2     | Título (superior) |
| 3     | Root        |
| 4     | Subimagem  |
| 5     | Áudio       |
| 6     | Ângulo       |
| 7     | Capítulo     |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os nomes de menu de DVD podem ser um pouco confusos. O menu título é outro nome para o menu Gerenciador de vídeo, o menu principal do disco inteiro; em geral, ele lista todos os conjuntos de títulos de vídeo disponíveis no disco. O menu raiz é o menu de um conjunto de título de vídeo, que pode conter um título ou um grupo de títulos. Todos os títulos em um conjunto de título compartilham os mesmos menus de subimagem, áudio e ângulo.

 

 



