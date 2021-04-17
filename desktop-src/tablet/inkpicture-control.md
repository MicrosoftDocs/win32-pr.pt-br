---
description: Tópico de referência para o controle InkPicture do Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Controle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749176"
---
# <a name="inkpicture-control"></a>Controle InkPicture

O controle [InkPicture](inkpicture-control-reference.md) permite que você coloque um formato de imagem (. jpg,. bmp,. png ou. gif) em um aplicativo ao qual os usuários possam adicionar tinta. Ele destina-se a cenários nos quais a tinta não precisa ser reconhecida como texto, mas é armazenada como tinta.

Os usuários adicionam tinta a uma camada transparente usando uma caneta. Os usuários podem redimensionar uma janela [InkPicture](inkpicture-control-reference.md) sem perder nenhuma informação de tinta, mesmo que a tinta seja cortada ao redimensionar.

O controle [InkPicture](inkpicture-control-reference.md) inclui suporte a impressão básica; no entanto, cabe a você implementar a visualização de impressão ou outros recursos de impressão avançados.

A implementação gerenciada (.NET Framework) do [InkPicture](/previous-versions/ms583740(v=vs.100)) herda da classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .

Por padrão, a tinta será colorida em preto se não estiver no modo de alto contraste; caso contrário, ele será definido como o valor atual de configuração de cor do sistema (COLOR \_ WINDOWTEXT). Além disso, por padrão, o [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) é **false**.

No controle [InkPicture](inkpicture-control-reference.md) , use o objeto [**Ink**](inkdisp-class.md) para carregar e salvar a tinta.

> [!Note]  
> Quando você define [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) para **excluir** ou **selecionar**, outros eventos (como o evento [**Stroke**](inkpicture-stroke.md) ) são disparados. Esses eventos serão úteis se você quiser implementar seus próprios modos de exclusão ou de seleção.

 

Para obter informações de referência detalhadas sobre o controle [InkPicture](inkpicture-control-reference.md) , consulte InkPicture.

As seções a seguir detalham o uso do controle [InkPicture](inkpicture-control-reference.md) :

-   [Trabalhando com imagens](working-with-pictures.md)
-   [Usando o InkPicture em versões anteriores do Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
