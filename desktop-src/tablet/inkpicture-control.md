---
description: Tópico de referência para o controle InkPicture para o Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Controle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451095"
---
# <a name="inkpicture-control"></a>Controle InkPicture

O [controle InkPicture](inkpicture-control-reference.md) permite que você coloque uma imagem (formato .jpg, .bmp, .png ou .gif) em um aplicativo ao que os usuários podem adicionar tinta. Ele destina-se a cenários em que a tinta não precisa ser reconhecida como texto, mas é armazenada como tinta.

Os usuários adicionam tinta a uma camada transparente usando uma caneta. Os usuários podem rea tamanho de [uma janela inkPicture](inkpicture-control-reference.md) sem perder nenhuma informação de tinta, mesmo que a tinta seja cortada ao reacortar.

O [controle InkPicture inclui](inkpicture-control-reference.md) suporte básico à impressão; no entanto, cabe a você implementar a visualização de impressão ou outros recursos avançados de impressão.

A implementação gerenciada (.NET Framework) [do InkPicture](/previous-versions/ms583740(v=vs.100)) herda da [classe PictureBox.](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1)

Por padrão, a tinta será colorida em preto se não estiver no modo de alto contraste; caso contrário, ele será definido como a configuração de cor atual do sistema (COLOR \_ WINDOWTEXT). Além disso, por [**padrão, FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) é **FALSE.**

No controle [InkPicture,](inkpicture-control-reference.md) use o [**objeto Ink**](inkdisp-class.md) para carregar e salvar tinta.

> [!Note]  
> Quando você definir [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) como **Excluir** ou **Selecionar**, outros eventos (como o [**evento Stroke)**](inkpicture-stroke.md) serão disparados. Esses eventos serão úteis se você quiser implementar seus próprios modos de exclusão ou seleção.

 

Para obter informações de referência detalhadas sobre o [controle InkPicture,](inkpicture-control-reference.md) consulte InkPicture.

As seções a seguir detalham o uso do [controle InkPicture:](inkpicture-control-reference.md)

-   [Trabalhando com imagens](working-with-pictures.md)
-   [Usando o InkPicture em versões anteriores do Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
