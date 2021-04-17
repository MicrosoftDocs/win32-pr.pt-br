---
description: Este tópico descreve como ajustar imagens usando a propriedade System. Windows. Forms. PictureBox. ModoTamanho e como exibir imagens no Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Trabalhando com imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813287"
---
# <a name="working-with-pictures"></a><span data-ttu-id="28028-103">Trabalhando com imagens</span><span class="sxs-lookup"><span data-stu-id="28028-103">Working with Pictures</span></span>

<span data-ttu-id="28028-104">Este tópico descreve como ajustar imagens usando a propriedade [System. Windows. Forms. PictureBox. ModoTamanho](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) e como exibir imagens no Microsoft Visual Studio .net.</span><span class="sxs-lookup"><span data-stu-id="28028-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="28028-105">A propriedade ModoTamanho</span><span class="sxs-lookup"><span data-stu-id="28028-105">The SizeMode Property</span></span>

<span data-ttu-id="28028-106">Você pode especificar como uma imagem se ajusta ao controle com a propriedade [ModoTamanho](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="28028-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="28028-107">A propriedade ModoTamanho está disponível na biblioteca gerenciada e na biblioteca de automação.</span><span class="sxs-lookup"><span data-stu-id="28028-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="28028-108">Com o ModoTamanho, você pode:</span><span class="sxs-lookup"><span data-stu-id="28028-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="28028-109">Redimensione as bordas de controle para se ajustar a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="28028-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="28028-110">Alongar uma imagem para ajustá-la às bordas do controle.</span><span class="sxs-lookup"><span data-stu-id="28028-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="28028-111">Centralizar uma imagem dentro das bordas do controle.</span><span class="sxs-lookup"><span data-stu-id="28028-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="28028-112">Ancorar uma imagem na área superior esquerda do controle sem redimensionar a imagem ou o controle (parte da imagem poderá não ser visível se você não redimensionar a imagem ou o controle).</span><span class="sxs-lookup"><span data-stu-id="28028-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="28028-113">Trabalhando com imagens no Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="28028-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="28028-114">Para exibir uma imagem em tempo de design no Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="28028-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="28028-115">Arraste um controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) em um formulário ou clique duas vezes no controle InkPicture na caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="28028-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="28028-116">Na janela **Propriedades** , selecione a propriedade **imagem** e clique no botão de reticências para abrir a caixa de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="28028-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="28028-117">Se você estiver procurando um tipo de arquivo específico (por exemplo, arquivos. jpg), selecione-o na caixa **arquivos do tipo** .</span><span class="sxs-lookup"><span data-stu-id="28028-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="28028-118">Selecione o arquivo que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="28028-118">Select the file you want to display.</span></span>

<span data-ttu-id="28028-119">Para limpar a imagem em tempo de design:</span><span class="sxs-lookup"><span data-stu-id="28028-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="28028-120">Na janela **Propriedades** , selecione a propriedade **imagem** e clique com o botão direito do mouse na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="28028-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="28028-121">Clique em **redefinir**.</span><span class="sxs-lookup"><span data-stu-id="28028-121">Click **Reset**.</span></span>

<span data-ttu-id="28028-122">O controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) é exibido por padrão sem nenhuma borda.</span><span class="sxs-lookup"><span data-stu-id="28028-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="28028-123">Você pode fornecer uma borda padrão ou tridimensional usando a propriedade [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) para distinguir a caixa InkPicture do restante do formulário, mesmo que ela não contenha nenhuma imagem.</span><span class="sxs-lookup"><span data-stu-id="28028-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="28028-124">Você pode exibir uma imagem em tempo de execução com o método [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) do objeto [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :</span><span class="sxs-lookup"><span data-stu-id="28028-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="28028-125">Você também pode incluir uma imagem de plano de fundo com a propriedade [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) do objeto de [imagem](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) herdado; no entanto, essa imagem não pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="28028-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
