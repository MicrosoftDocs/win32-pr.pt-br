---
description: Este tópico descreve como ajustar imagens usando o sistema. Windows. propriedade Forms. PictureBox. modotamanho e como exibir imagens no Microsoft Visual Studio .net.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Trabalhando com imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6e3331d384f30084082e8ef29c5a3a5b44232843bc834a8282bf1786a088d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449171"
---
# <a name="working-with-pictures"></a>Trabalhando com imagens

Este tópico descreve como ajustar imagens usando o [System. Windows. propriedade Forms. PictureBox. modotamanho](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) e como exibir imagens no Microsoft Visual Studio .net.

## <a name="the-sizemode-property"></a>A propriedade ModoTamanho

Você pode especificar como uma imagem se ajusta ao controle com a propriedade [ModoTamanho](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) . A propriedade ModoTamanho está disponível na biblioteca gerenciada e na biblioteca de automação. Com o ModoTamanho, você pode:

-   Redimensione as bordas de controle para se ajustar a uma imagem.
-   Alongar uma imagem para ajustá-la às bordas do controle.
-   Centralizar uma imagem dentro das bordas do controle.
-   Ancorar uma imagem na área superior esquerda do controle sem redimensionar a imagem ou o controle (parte da imagem poderá não ser visível se você não redimensionar a imagem ou o controle).

## <a name="working-with-pictures-in-visual-studio-net"></a>trabalhando com imagens no Visual Studio .net

para exibir uma imagem em tempo de design no Visual Studio .net:

1.  Arraste um controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) em um formulário ou clique duas vezes no controle InkPicture na caixa de ferramentas.
2.  Na janela **Propriedades** , selecione a propriedade **imagem** e clique no botão de reticências para abrir a caixa de diálogo **abrir** .
3.  Se você estiver procurando um tipo de arquivo específico (por exemplo, .jpg arquivos), selecione-o na caixa **arquivos do tipo** .
4.  Selecione o arquivo que você deseja exibir.

Para limpar a imagem em tempo de design:

1.  Na janela **Propriedades** , selecione a propriedade **imagem** e clique com o botão direito do mouse na imagem em miniatura.
2.  Clique em **redefinir**.

O controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) é exibido por padrão sem nenhuma borda. Você pode fornecer uma borda padrão ou tridimensional usando a propriedade [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) para distinguir a caixa InkPicture do restante do formulário, mesmo que ela não contenha nenhuma imagem.

Você pode exibir uma imagem em tempo de execução com o método [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) do objeto [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



Você também pode incluir uma imagem de plano de fundo com a propriedade [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) do objeto de [imagem](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) herdado; no entanto, essa imagem não pode ser redimensionada.

 

 
