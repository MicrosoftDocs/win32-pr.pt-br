---
description: O método ShowMenu exibe o menu especificado na tela.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Método ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb9135e2999675dc46774f15ee79afd835085b40fe210d0ca1cfd173f8a99fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050506"
---
# <a name="showmenu-method"></a>Método ShowMenu

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

Especifica a ID do menu como um Inteiro.



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

Nomes de menu de DVD podem ser um pouco confusos. O menu de título é outro nome para o Menu gerenciador de vídeo, o menu principal para todo o disco; geralmente lista todos os conjuntos de títulos de vídeo disponíveis no disco. O menu raiz é o menu para um conjunto de títulos de vídeo, que pode conter um título ou um grupo de títulos. Todos os títulos em um conjunto de título compartilham os mesmos menus Subpicture, Audio e Angle.

 

 



