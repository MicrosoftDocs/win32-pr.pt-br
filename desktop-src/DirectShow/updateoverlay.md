---
description: O evento UpdateOverlay é enviado quando a superfície de sobreposição foi movida ou redimensionada ou sua chave de cor foi alterada.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757567"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O evento **UpdateOverlay** é enviado quando a superfície de sobreposição foi movida ou redimensionada ou sua chave de cor foi alterada.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Comentários

Os aplicativos nunca devem se preocupar com a superfície de sobreposição sendo redimensionada ou movida. Tudo isso é tratado internamente. Mas esse evento também é enviado quando a chave de cor é alterada. Isso significa que, se um aplicativo estiver hospedando MSWebDVD como um controle sem janela e exibir botões flutuantes sobre a superfície de vídeo no modo de tela inteira, ele deverá responder a esse evento obtendo o novo valor da propriedade **COLORKEY** para que ele possa desenhar os botões corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

 




