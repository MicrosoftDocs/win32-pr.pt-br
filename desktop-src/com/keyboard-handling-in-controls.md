---
title: Manipulação de teclado em controles
description: Manipulação de teclado em controles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811600"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="fb544-103">Manipulação de teclado em controles</span><span class="sxs-lookup"><span data-stu-id="fb544-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="fb544-104">O suporte ao manuseio de teclado para a funcionalidade a seguir é altamente recomendável, embora seja reconhecido que ele não seja aplicável a todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="fb544-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="fb544-105">Suporte para \_ bits de status OLEMISC ACTSLIKELABEL e OLEMISC \_ ACTSLIKEBUTTON.</span><span class="sxs-lookup"><span data-stu-id="fb544-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="fb544-106">Implementando a propriedade de ambiente DisplayAsDefault (se existir, ela pode retornar **false**).</span><span class="sxs-lookup"><span data-stu-id="fb544-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="fb544-107">Implementando a manipulação de guias, incluindo a ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="fb544-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="fb544-108">Alguns contêineres usarão controles ActiveX em cenários tradicionais de documento composto.</span><span class="sxs-lookup"><span data-stu-id="fb544-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="fb544-109">Por exemplo, uma planilha pode permitir que um usuário insira um controle ActiveX em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="fb544-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="fb544-110">Nesses cenários, o contêiner faria o manuseio do teclado de forma diferente, pois a interface do teclado deve permanecer consistente com as expectativas do usuário de uma planilha.</span><span class="sxs-lookup"><span data-stu-id="fb544-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="fb544-111">A documentação para esses produtos deve informar os usuários sobre as diferenças na manipulação de controle nesses diferentes cenários.</span><span class="sxs-lookup"><span data-stu-id="fb544-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="fb544-112">Outros contêineres devem se esforçar para honrar a funcionalidade acima, incluindo a manipulação de mnemônico.</span><span class="sxs-lookup"><span data-stu-id="fb544-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb544-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb544-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb544-114">Contêineres</span><span class="sxs-lookup"><span data-stu-id="fb544-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




