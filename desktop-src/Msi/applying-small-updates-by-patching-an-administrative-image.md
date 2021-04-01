---
description: Uma instalação administrativa cria uma imagem de origem de um aplicativo ou produto em uma rede.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921515"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="cf8c9-103">Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa</span><span class="sxs-lookup"><span data-stu-id="cf8c9-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="cf8c9-104">Uma [instalação administrativa](administrative-installation.md) cria uma imagem de origem de um aplicativo ou produto em uma rede.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="cf8c9-105">Os usuários em um grupo de trabalho que têm acesso a essa imagem administrativa podem instalar o produto dessa fonte.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="cf8c9-106">A atualização do aplicativo para esse grupo de trabalho é feita em duas etapas:</span><span class="sxs-lookup"><span data-stu-id="cf8c9-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="cf8c9-107">Primeiro, o patch de atualização pequena pode ser aplicado à imagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="cf8c9-108">Em segundo lugar, as alterações na atualização pequena precisam ser propagadas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="cf8c9-109">**Para aplicar um patch de atualização pequeno a uma imagem administrativa**</span><span class="sxs-lookup"><span data-stu-id="cf8c9-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="cf8c9-110">Obtenha a pequena atualização na forma de um [pacote de patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="cf8c9-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="cf8c9-111">Por exemplo, a pequena atualização chamada patch. msp.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="cf8c9-112">Obtenha o caminho para a imagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="cf8c9-113">A partir da linha de comando, use:</span><span class="sxs-lookup"><span data-stu-id="cf8c9-113">From the command line use:</span></span>

    <span data-ttu-id="cf8c9-114">**msiexec/a** *\[ caminho para o arquivo \] . msi da imagem administrativa* **/p** *patch. msp*</span><span class="sxs-lookup"><span data-stu-id="cf8c9-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="cf8c9-115">Isso atualiza os arquivos do aplicativo e o arquivo. msi da imagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="cf8c9-116">Para obter uma lista das opções que podem ser usadas com Msiexec.exe, consulte [Opções de linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="cf8c9-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="cf8c9-117">Windows Installer determina automaticamente se a imagem administrativa está usando nomes de arquivo curtos e define a propriedade [**SHORTFILENAMES**](shortfilenames.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8c9-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="cf8c9-118">A imagem administrativa resultante é a mesma que a produzida por uma instalação administrativa usando um CD-ROM completo do produto que inclui a atualização.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="cf8c9-119">Quando novos usuários instalam o aplicativo dessa fonte, eles recebem o aplicativo atualizado.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="cf8c9-120">**Para propagar a pequena atualização para o grupo de trabalho**</span><span class="sxs-lookup"><span data-stu-id="cf8c9-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="cf8c9-121">Os membros do grupo de trabalho obtêm as alterações reinstalando o aplicativo da imagem administrativa usando o procedimento descrito em [aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="cf8c9-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



