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
# <a name="inkpicture-control"></a><span data-ttu-id="0ff6c-103">Controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="0ff6c-103">InkPicture Control</span></span>

<span data-ttu-id="0ff6c-104">O controle [InkPicture](inkpicture-control-reference.md) permite que você coloque um formato de imagem (. jpg,. bmp,. png ou. gif) em um aplicativo ao qual os usuários possam adicionar tinta.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="0ff6c-105">Ele destina-se a cenários nos quais a tinta não precisa ser reconhecida como texto, mas é armazenada como tinta.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="0ff6c-106">Os usuários adicionam tinta a uma camada transparente usando uma caneta.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="0ff6c-107">Os usuários podem redimensionar uma janela [InkPicture](inkpicture-control-reference.md) sem perder nenhuma informação de tinta, mesmo que a tinta seja cortada ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="0ff6c-108">O controle [InkPicture](inkpicture-control-reference.md) inclui suporte a impressão básica; no entanto, cabe a você implementar a visualização de impressão ou outros recursos de impressão avançados.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="0ff6c-109">A implementação gerenciada (.NET Framework) do [InkPicture](/previous-versions/ms583740(v=vs.100)) herda da classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="0ff6c-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="0ff6c-110">Por padrão, a tinta será colorida em preto se não estiver no modo de alto contraste; caso contrário, ele será definido como o valor atual de configuração de cor do sistema (COLOR \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="0ff6c-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="0ff6c-111">Além disso, por padrão, o [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) é **false**.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="0ff6c-112">No controle [InkPicture](inkpicture-control-reference.md) , use o objeto [**Ink**](inkdisp-class.md) para carregar e salvar a tinta.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="0ff6c-113">Quando você define [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) para **excluir** ou **selecionar**, outros eventos (como o evento [**Stroke**](inkpicture-stroke.md) ) são disparados.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="0ff6c-114">Esses eventos serão úteis se você quiser implementar seus próprios modos de exclusão ou de seleção.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="0ff6c-115">Para obter informações de referência detalhadas sobre o controle [InkPicture](inkpicture-control-reference.md) , consulte InkPicture.</span><span class="sxs-lookup"><span data-stu-id="0ff6c-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="0ff6c-116">As seções a seguir detalham o uso do controle [InkPicture](inkpicture-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="0ff6c-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="0ff6c-117">Trabalhando com imagens</span><span class="sxs-lookup"><span data-stu-id="0ff6c-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="0ff6c-118">Usando o InkPicture em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="0ff6c-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
