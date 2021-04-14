---
title: Operações de DrawDib
description: Operações de DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, sobre
- DrawDib, acessando
- DrawDib, abrindo
- DrawDib, operações
- DrawDib, contexto do dispositivo (DC)
- DC (contexto do dispositivo)
- Função DrawDibOpen
- Função DrawDibClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453723"
---
# <a name="drawdib-operations"></a><span data-ttu-id="0ac9e-111">Operações de DrawDib</span><span class="sxs-lookup"><span data-stu-id="0ac9e-111">DrawDib Operations</span></span>

<span data-ttu-id="0ac9e-112">Você pode acessar o grupo inteiro de funções DrawDib usando a função [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) .</span><span class="sxs-lookup"><span data-stu-id="0ac9e-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="0ac9e-113">Essa função carrega a DLL (biblioteca de vínculo dinâmico), aloca recursos de memória, cria um DrawDib (contexto de dispositivo) e mantém uma contagem de referência do número de controladores de domínio que são inicializados.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="0ac9e-114">O **DrawDibOpen** também retorna um identificador do novo DC que você usa com as outras funções DrawDib.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="0ac9e-115">Você pode liberar um DrawDib DC ao terminar de usá-lo usando a função [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) .</span><span class="sxs-lookup"><span data-stu-id="0ac9e-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="0ac9e-116">**DrawDibClose** também decrementa a contagem de referência dos aplicativos que acessam a dll.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="0ac9e-117">A chamada para **DrawDibClose** deve ser a última função DrawDib em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="0ac9e-118">Você pode criar quantos DCs DrawDib desejar.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="0ac9e-119">Você pode usar vários DCs DrawDib para desenhar vários bitmaps simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="0ac9e-120">Você também pode criar vários DCs DrawDib, cada um com características exclusivas, para que seu aplicativo possa escolher e, em seguida, usar o controlador de domínio com as configurações mais apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="0ac9e-121">Por exemplo, você pode criar dois DCs DrawDib em um aplicativo: um que exibe uma imagem em sua resolução normal e o outro que exibe uma parte ampliada da imagem.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="0ac9e-122">Para executar com eficiência, as funções DrawDib exigem informações sobre o adaptador de vídeo e seu driver.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="0ac9e-123">O perfil de exibição é obtido executando uma série de testes no adaptador de vídeo na primeira vez que a DLL que contém as funções DrawDib é acessada.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="0ac9e-124">As funções DrawDib usam essas informações para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="0ac9e-125">Você pode repetir esses testes quando necessário usando a função [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .</span><span class="sxs-lookup"><span data-stu-id="0ac9e-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="0ac9e-126">Recuperar e armazenar o perfil de exibição normalmente é uma ocorrência única.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="0ac9e-127">Se, no entanto, as informações de perfil forem excluídas ou outro driver de vídeo estiver instalado no sistema, o DrawDib executará novamente os testes.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0ac9e-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ac9e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ac9e-129">Sobre as funções DrawDib</span><span class="sxs-lookup"><span data-stu-id="0ac9e-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




