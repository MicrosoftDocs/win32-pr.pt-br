---
description: Criando o arquivo de recurso de idioma base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Criando o arquivo de recurso de idioma base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011634"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="4b8d7-103">Criando o arquivo de recurso de idioma base</span><span class="sxs-lookup"><span data-stu-id="4b8d7-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="4b8d7-104">Os recursos dos elementos da interface do usuário são definidos para a linguagem básica à qual o aplicativo dá suporte, por exemplo, inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="4b8d7-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="4b8d7-105">Um exemplo de um arquivo de recurso do Win32 PE é um arquivo. rc, criado usando o compilador RC.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="4b8d7-106">Para obter detalhes sobre a criação do arquivo. rc, consulte [sobre os arquivos de recurso](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="4b8d7-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="4b8d7-107">Se estiver usando um arquivo. rc para os recursos de idioma base, você terá a opção de usar um arquivo de configuração de recurso para uma representação XML dos dados de configuração de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="4b8d7-108">Para criar esse arquivo, consulte [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="4b8d7-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="4b8d7-109">Você também pode usar um arquivo PE não Win32 para definir recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="4b8d7-110">Por exemplo, você pode usar um arquivo. xml ou. txt para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="4b8d7-111">Ao definir recursos de idioma base usando um arquivo PE não Win32, você não pode usar o compilador RC para definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="4b8d7-112">Em vez disso, você define seu próprio formato de recurso e seu aplicativo deve fornecer sua própria funcionalidade para localizar e carregar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4b8d7-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b8d7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b8d7-114">Preparando recursos</span><span class="sxs-lookup"><span data-stu-id="4b8d7-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="4b8d7-115">Preparando um arquivo de configuração de recurso</span><span class="sxs-lookup"><span data-stu-id="4b8d7-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
