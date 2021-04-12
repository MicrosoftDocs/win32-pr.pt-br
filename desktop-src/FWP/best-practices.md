---
title: Práticas recomendadas (plataforma de filtragem do Windows)
description: A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API da Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499211"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="a0db0-103">Práticas recomendadas (plataforma de filtragem do Windows)</span><span class="sxs-lookup"><span data-stu-id="a0db0-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="a0db0-104">A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API da Windows Filtering Platform (WFP).</span><span class="sxs-lookup"><span data-stu-id="a0db0-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="a0db0-105">Use sessões dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="a0db0-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="a0db0-106">Muitos aplicativos adicionam objetos de política de filtragem no início e, em seguida, excluem esses objetos em stop.</span><span class="sxs-lookup"><span data-stu-id="a0db0-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="a0db0-107">Usando uma sessão dinâmica, você garante que esses objetos sejam excluídos mesmo se o aplicativo falhar.</span><span class="sxs-lookup"><span data-stu-id="a0db0-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="a0db0-108">Além disso, simplesmente fechar o identificador do mecanismo em Stop é mais eficiente do que fazer chamadas individuais para excluir cada objeto.</span><span class="sxs-lookup"><span data-stu-id="a0db0-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="a0db0-109">Trate os tempos limite da transação normalmente ou defina a sessão **txnWaitTimeoutInMSec** como infinito para evitar tempos limite.</span><span class="sxs-lookup"><span data-stu-id="a0db0-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="a0db0-110">Mesmo que você não use transações explícitas, a maioria das chamadas ainda será executada em uma transação implícita e, portanto, poderá atingir o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a0db0-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="a0db0-111">Use transações explícitas para combinar operações de adição ou exclusão relacionadas em uma única transação.</span><span class="sxs-lookup"><span data-stu-id="a0db0-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="a0db0-112">Isso é mais eficiente e torna mais fácil limpar resultados parciais em caminhos de erro.</span><span class="sxs-lookup"><span data-stu-id="a0db0-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="a0db0-113">Use cadeias de caracteres compatíveis com o MUI.</span><span class="sxs-lookup"><span data-stu-id="a0db0-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="a0db0-114">Todas as cadeias de caracteres localizáveis são armazenadas em uma estrutura de dados comum: [**FWPM \_ Exibir \_ data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="a0db0-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="a0db0-115">As cadeias de caracteres nessa estrutura podem ser cadeias de caracteres indiretas do tipo com suporte do [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="a0db0-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="a0db0-116">Antes que uma estrutura **\_ \_ data0 de exibição de FWPM** seja retornada por qualquer uma das funções, as cadeias de caracteres indiretas são resolvidas para o recurso de cadeia de caracteres especificado usando a localidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="a0db0-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="a0db0-117">Associar todos os objetos a um provedor.</span><span class="sxs-lookup"><span data-stu-id="a0db0-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="a0db0-118">Quando vários provedores são instalados no sistema, isso torna mais fácil para as ferramentas de diagnóstico determinar quem adicionou o quê.</span><span class="sxs-lookup"><span data-stu-id="a0db0-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="a0db0-119">Adicione filtros a sua própria subcamada.</span><span class="sxs-lookup"><span data-stu-id="a0db0-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="a0db0-120">Depois que um filtro de terminação em uma subcamada for atingido, nenhum filtro será avaliado nessa subcamada.</span><span class="sxs-lookup"><span data-stu-id="a0db0-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="a0db0-121">Portanto, se você adicionar seus filtros à mesma subcamada como outro provedor, poderá impedir que os filtros uns dos outros sejam invocados, resultando em resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="a0db0-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="a0db0-122">Use a ALE (aplicação de camada de aplicativo) em vez da filtragem orientada por pacotes.</span><span class="sxs-lookup"><span data-stu-id="a0db0-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="a0db0-123">A filtragem na camada de pacote está lenta.</span><span class="sxs-lookup"><span data-stu-id="a0db0-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="a0db0-124">Filtre os erros de ICMP e os eventos RST antes que eles sejam gerados.</span><span class="sxs-lookup"><span data-stu-id="a0db0-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="a0db0-125">Isso é mais eficiente para filtrar esses eventos depois que eles são gerados.</span><span class="sxs-lookup"><span data-stu-id="a0db0-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="a0db0-126">Execute a inspeção de pacotes na camada de dados de fluxo/datagrama em vez de na camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="a0db0-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="a0db0-127">Isso se aplica ao desenvolvimento de textos explicativos.</span><span class="sxs-lookup"><span data-stu-id="a0db0-127">This applies to developing callouts.</span></span> <span data-ttu-id="a0db0-128">Para obter mais informações, consulte [considerações de programação de driver de texto explicativo](/windows-hardware/drivers/network/callout-driver-programming-considerations) no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="a0db0-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="a0db0-129">Considere as implicações de desempenho ao usar filtros complexos.</span><span class="sxs-lookup"><span data-stu-id="a0db0-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="a0db0-130">A partir do Windows 7 e do Windows Server 2008 R2, os filtros podem ser criados com várias condições que usam a mesma chave de campo.</span><span class="sxs-lookup"><span data-stu-id="a0db0-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="a0db0-131">Isso permite que políticas complexas sejam criadas com menos filtros.</span><span class="sxs-lookup"><span data-stu-id="a0db0-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="a0db0-132">No entanto, esses filtros complexos podem incorrer em um desempenho mais lento para o mecanismo de filtro WFP classificar.</span><span class="sxs-lookup"><span data-stu-id="a0db0-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="a0db0-133">Deve-se fazer uma avaliação para determinar se o uso desses filtros causa um efeito adverso no desempenho geral da solução.</span><span class="sxs-lookup"><span data-stu-id="a0db0-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
