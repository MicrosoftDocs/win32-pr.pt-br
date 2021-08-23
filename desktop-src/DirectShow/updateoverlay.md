---
description: O evento UpdateOverlay é enviado quando a superfície de sobreposição foi movida ou recalizada ou sua chave de cor foi alterada.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205b4ca002ec06862b006dc3e3b6facec2f5cb7f0ffb92f3e5a65bc2bb0a161c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650817"
---
# <a name="updateoverlay"></a>Updateoverlay

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O **evento UpdateOverlay** é enviado quando a superfície de sobreposição foi movida ou recalizada ou sua chave de cor foi alterada.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Comentários

Os aplicativos nunca devem se preocupar com a superfície de sobreposição que está sendo relizada ou movida. Tudo isso é tratado internamente. Mas esse evento também é enviado quando a chave de cor é muda. Isso significa que, se um aplicativo estiver hospedando MSWebDVD como um controle sem janela e exibindo botões flutuantes sobre a superfície de vídeo no modo de tela inteira, ele deverá responder a esse evento ao obter o novo valor da propriedade **ColorKey** para que ele possa desenhar os botões corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

 




