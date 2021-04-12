---
title: Redimensionando a caixa de diálogo de aquisição de licença
description: Redimensionando a caixa de diálogo de aquisição de licença
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, caixa de diálogo redimensionar a aquisição de licença
- Caixa de diálogo Windows Media Player, aquisição de licença
- Windows Media Player, DRM_LicenseAcqURL atributo
- caixa de diálogo redimensionar a aquisição de licença
- Caixa de diálogo aquisição de licença
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364200"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="9ea0b-109">Redimensionando a caixa de diálogo de aquisição de licença</span><span class="sxs-lookup"><span data-stu-id="9ea0b-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="9ea0b-110">Você pode acrescentar parâmetros de cadeia de caracteres de consulta à URL fornecida para o atributo **\_ LicenseAcqURL do DRM** para especificar um tamanho para a caixa de diálogo de aquisição de licença do Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="9ea0b-111">A tabela a seguir lista os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="9ea0b-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ea0b-112">Parameter</span></span> | <span data-ttu-id="9ea0b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ea0b-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="9ea0b-114">*DlgX*</span><span class="sxs-lookup"><span data-stu-id="9ea0b-114">*DlgX*</span></span>    | <span data-ttu-id="9ea0b-115">Especifica a largura da caixa de diálogo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="9ea0b-116">*DlgY*</span><span class="sxs-lookup"><span data-stu-id="9ea0b-116">*DlgY*</span></span>    | <span data-ttu-id="9ea0b-117">Especifica a altura da caixa de diálogo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="9ea0b-118">Por exemplo, a seguinte URL de aquisição de licença faria com que a caixa de diálogo de aquisição de licença fosse aberta com um tamanho de 800 por 600 pixels:</span><span class="sxs-lookup"><span data-stu-id="9ea0b-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="9ea0b-119">O tamanho máximo da caixa de diálogo nunca excederá as dimensões da tela atual menos 20 pixels.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="9ea0b-120">O tamanho mínimo é 333 x 210 pixels (o tamanho padrão).</span><span class="sxs-lookup"><span data-stu-id="9ea0b-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="9ea0b-121">Esse recurso requer o Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea0b-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea0b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ea0b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea0b-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="9ea0b-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




