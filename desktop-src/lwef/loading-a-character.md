---
title: Carregando um caractere
description: Carregando um caractere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635861"
---
# <a name="loading-a-character"></a><span data-ttu-id="50965-103">Carregando um caractere</span><span class="sxs-lookup"><span data-stu-id="50965-103">Loading a Character</span></span>

<span data-ttu-id="50965-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="50965-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="50965-105">Para animar um caractere, você deve primeiro carregar o caractere.</span><span class="sxs-lookup"><span data-stu-id="50965-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="50965-106">Use o método [**Load**](load-method.md) para carregar os dados do caractere.</span><span class="sxs-lookup"><span data-stu-id="50965-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="50965-107">O Microsoft Agent dá suporte a dois formatos de dados de caractere e animação: um único arquivo estruturado e arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="50965-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="50965-108">Normalmente, você usa o formato de arquivo único (. ACS) quando os dados são armazenados localmente.</span><span class="sxs-lookup"><span data-stu-id="50965-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="50965-109">O formato de vários arquivos (. ACF,. ACA) funciona melhor quando você deseja baixar animações individualmente, como ao acessar animações de um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="50965-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="50965-110">Um aplicativo cliente pode carregar apenas uma única instância do mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="50965-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="50965-111">Qualquer tentativa de carregar o mesmo caractere mais de uma vez falhará.</span><span class="sxs-lookup"><span data-stu-id="50965-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="50965-112">No entanto, um aplicativo pode ter várias instâncias do mesmo caractere carregado fornecendo conexões separadas ao Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="50965-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="50965-113">Por exemplo, um aplicativo pode carregar o mesmo caractere de duas cópias do controle do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="50965-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="50965-114">Você também pode definir seus próprios caracteres para uso com o Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="50965-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="50965-115">Você pode usar qualquer ferramenta de renderização que preferir para criar as imagens, desde que você acabe com arquivos de formato de bitmap do Windows.</span><span class="sxs-lookup"><span data-stu-id="50965-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="50965-116">Para montar e compilar as imagens de um caractere em animações para uso com o Microsoft Agent, use o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="50965-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="50965-117">Essa ferramenta permite que você defina as propriedades padrão de um caractere, bem como definir animações para o caractere.</span><span class="sxs-lookup"><span data-stu-id="50965-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="50965-118">O editor de caracteres do Microsoft Agent também permite que você selecione o formato de arquivo apropriado ao criar um caractere.</span><span class="sxs-lookup"><span data-stu-id="50965-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




