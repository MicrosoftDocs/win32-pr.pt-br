---
description: Usando as classes base do DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Usando as classes base do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170271"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="8b7ce-103">Usando as classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b7ce-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="8b7ce-104">Para usar as classes base no DirectShow, você deve criar e vincular a biblioteca de classes base.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="8b7ce-105">A biblioteca de classes base é fornecida como um exemplo de SDK no Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="8b7ce-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="8b7ce-106">O local exato depende da versão do SDK que você instalou, mas o caminho relativo é:</span><span class="sxs-lookup"><span data-stu-id="8b7ce-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="8b7ce-107">*(Raiz de exemplos do SDK)* \\ BaseClasses do DirectShow \\</span><span class="sxs-lookup"><span data-stu-id="8b7ce-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="8b7ce-108">Cabeçalho: Streams. h</span><span class="sxs-lookup"><span data-stu-id="8b7ce-108">Header: Streams.h</span></span>

<span data-ttu-id="8b7ce-109">Biblioteca: o exemplo compila versões de varejo e de depuração da biblioteca:</span><span class="sxs-lookup"><span data-stu-id="8b7ce-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="8b7ce-110">Versão de varejo: Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="8b7ce-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="8b7ce-111">Versão de depuração: Strmbasd. lib.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="8b7ce-112">Para obter mais informações sobre como configurar o ambiente de compilação, consulte [Configurando o ambiente de compilação](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ce-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="8b7ce-113">Símbolos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="8b7ce-113">Preprocessor Symbols</span></span>

<span data-ttu-id="8b7ce-114">Quando você inclui o arquivo de cabeçalho Streams. h, os seguintes símbolos de pré-processador têm um significado especial:</span><span class="sxs-lookup"><span data-stu-id="8b7ce-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="8b7ce-115">PERF: reservado.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-115">PERF: Reserved.</span></span> <span data-ttu-id="8b7ce-116">Não use este símbolo de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="8b7ce-117">VFWROBUST: habilita a validação de ponteiro no varejo.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="8b7ce-118">Para obter mais informações, consulte [macros de validação de ponteiro](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ce-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="8b7ce-119">Em compilações de depuração, não é necessário definir VFWROBUST.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="8b7ce-120">No Windows Vista e posterior, as macros de validação do ponteiro estão vazias.</span><span class="sxs-lookup"><span data-stu-id="8b7ce-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 



