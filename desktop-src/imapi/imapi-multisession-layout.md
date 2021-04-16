---
title: Layout de várias sessões do IMAPi
description: O IMAPi fornece aos desenvolvedores de aplicativos a capacidade de criar imagens do sistema de arquivos ISO 9660 e UDF e gravá-las em CD, DVD e Blu-Ray \ 8482; mídia óptica.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104557041"
---
# <a name="imapi-multisession-layout"></a><span data-ttu-id="df2d0-103">Layout de várias sessões do IMAPi</span><span class="sxs-lookup"><span data-stu-id="df2d0-103">IMAPI Multisession Layout</span></span>

<span data-ttu-id="df2d0-104">O IMAPi fornece aos desenvolvedores de aplicativos a capacidade de criar imagens do sistema de arquivos ISO 9660 e UDF e gravá-las em CD, DVD e Blu-Ray™ mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="df2d0-104">IMAPI provides application developers with the ability to create ISO 9660 and UDF file system images and burn them onto CD, DVD and Blu-Ray™ optical media.</span></span> <span data-ttu-id="df2d0-105">Com o Windows 7, o IMAPi fornece suporte adicional para a gravação de várias sessões em DVD e Blu-Ray™ mídia regravável.</span><span class="sxs-lookup"><span data-stu-id="df2d0-105">With Windows 7, IMAPI provides additional support for multisession burning on DVD and Blu-Ray™ rewritable media.</span></span>

<span data-ttu-id="df2d0-106">A documentação a seguir detalha o layout do disco que o IMAPi utiliza para implementar várias sessões.</span><span class="sxs-lookup"><span data-stu-id="df2d0-106">The following documentation details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="df2d0-107">Essas informações devem ser usadas para garantir a interoperabilidade entre o IMAPi e outros softwares de gravação, além de permitir que os desenvolvedores desse software criem imagens de disco de várias sessões compatíveis com o IMAPi.</span><span class="sxs-lookup"><span data-stu-id="df2d0-107">This information should be used to ensure interoperability between IMAPI and other burning software as well as allow the developers of this software to create IMAPI-compatible multisession disc images.</span></span>

> [!Note]  
> <span data-ttu-id="df2d0-108">Para obter um exemplo detalhando a criação de um disco de várias sessões, consulte [criando um disco de várias sessões](creating-a-multisession-disc.md).</span><span class="sxs-lookup"><span data-stu-id="df2d0-108">For an example detailing the creation of a multisession disc, see [Creating a Multisession Disc](creating-a-multisession-disc.md).</span></span>

 

## <a name="multisession-on-sequential-media"></a><span data-ttu-id="df2d0-109">Várias sessões em mídia sequencial</span><span class="sxs-lookup"><span data-stu-id="df2d0-109">Multisession on Sequential Media</span></span>

<span data-ttu-id="df2d0-110">A implementação de IMAPi de várias sessões em mídia sequencial tem suporte para uso com mídia de CD-R, CD-RW, DVD-R, DVD + R e Blu-Ray™.</span><span class="sxs-lookup"><span data-stu-id="df2d0-110">The IMAPI implementation of multisession on sequential media is supported for use with CD-R, CD-RW, DVD-R, DVD+R and Blu-Ray™ media.</span></span> <span data-ttu-id="df2d0-111">O IMAPi usa o modo de gravação de sessão em uma vez para o CD-RW e, como resultado, nesse cenário, o formato é considerado um tipo de mídia sequencial.</span><span class="sxs-lookup"><span data-stu-id="df2d0-111">IMAPI uses the Session-At-Once recording mode for CD-RW, and as a result, in this scenario, the format is considered a sequential media type.</span></span>

<span data-ttu-id="df2d0-112">Em um cenário que envolve a multisessão em mídia sequencial usando UDF, o IMAPi grava as estruturas de âncora (o descritor de volume de âncora UDF-AVDP), estruturas de volume (sequência de descritor de volume UDF-VDS) e as estruturas de metadados do sistema de arquivos (descritor de conjunto de arquivos UDF-FSD) no início de cada nova sessão, conforme descrita no</span><span class="sxs-lookup"><span data-stu-id="df2d0-112">In a scenario involving multisession on sequential media using UDF, IMAPI writes out the anchor structures (UDF Anchor Volume Descriptor Pointer - AVDP), volume structures (UDF Volume Descriptor Sequence - VDS) , and the file system metadata structures (UDF File Set Descriptor - FSD) at the start of every new session as outlined in the following diagram:</span></span>

![Diagrama que mostra a estrutura de metadados do sistema de arquivos com o "ponto de montagem da importação/F S" indicado com uma seta vermelha na "âncora" da sessão física 2.](images/multises1.png)

> [!Note]  
> <span data-ttu-id="df2d0-114">Esta figura ilustra o layout do disco IMAPi ao usar o UDF 2,50 com metadados redundantes.</span><span class="sxs-lookup"><span data-stu-id="df2d0-114">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="df2d0-115">Os dados armazenados em mídias gravadas em sequência consistem em um número de sessões físicas.</span><span class="sxs-lookup"><span data-stu-id="df2d0-115">The data stored on sequentially recorded media consists of a number of physical sessions.</span></span> <span data-ttu-id="df2d0-116">Cada sessão contém um sistema de arquivos completo que representa os dados do usuário como um conjunto de arquivos organizados em diretórios.</span><span class="sxs-lookup"><span data-stu-id="df2d0-116">Each session contains a complete file system representing user data as a set of files organized in directories.</span></span> <span data-ttu-id="df2d0-117">Os metadados do sistema de arquivos consistem em várias estruturas de dados organizadas hierarquicamente.</span><span class="sxs-lookup"><span data-stu-id="df2d0-117">The file system metadata consists of a number of hierarchically organized data structures.</span></span> <span data-ttu-id="df2d0-118">Na parte superior da hierarquia residem as estruturas de âncora (AVDP) em endereços de bloco lógico predefinidos (LBAs).</span><span class="sxs-lookup"><span data-stu-id="df2d0-118">At the top of the hierarchy reside anchor structures (AVDP) located at pre-defined Logical Block Addresses (LBAs).</span></span> <span data-ttu-id="df2d0-119">As estruturas de âncora especificam os locais das estruturas de próximo nível que não têm endereços predefinidos.</span><span class="sxs-lookup"><span data-stu-id="df2d0-119">The anchor structures specify the locations of the next level structures which do not have predefined addresses.</span></span> <span data-ttu-id="df2d0-120">O próximo nível de hierarquia após as estruturas de ancoragem contém as estruturas de volume (VDS) que descrevem as propriedades do volume e referenciando as FSD (estruturas de metadados do sistema de arquivos) que, por sua vez, descrevem arquivos e diretórios individuais.</span><span class="sxs-lookup"><span data-stu-id="df2d0-120">The next level of hierarchy after anchor structures contains the volume structures (VDS) that describe the properties of the volume and referencing the file system metadata structures (FSD), which in turn describe individual files and directories.</span></span>

## <a name="multisession-on-rewritable-media"></a><span data-ttu-id="df2d0-121">Várias sessões em mídia regravável</span><span class="sxs-lookup"><span data-stu-id="df2d0-121">Multisession on Rewritable Media</span></span>

<span data-ttu-id="df2d0-122">A abordagem para mídia sequencial descrita na seção anterior é incompatível com mídia regravável (não sequencial).</span><span class="sxs-lookup"><span data-stu-id="df2d0-122">The approach for sequential media outlined in the previous section is incompatible with rewritable (non-sequential) media.</span></span> <span data-ttu-id="df2d0-123">Esses formatos de mídia incluem DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ regravável e outras mídias graváveis aleatórias, como discos Iomega REV.</span><span class="sxs-lookup"><span data-stu-id="df2d0-123">These media formats include DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable and other random writable media, such as Iomega REV disks.</span></span> <span data-ttu-id="df2d0-124">A mídia regravável não dá suporte ao conceito de sessões físicas correspondentes às sessões lógicas, que são incrementos individuais confirmados por um aplicativo de mestre.</span><span class="sxs-lookup"><span data-stu-id="df2d0-124">Rewritable media does not support the concept of physical sessions corresponding to logical sessions, which are individual increments committed by a mastering application.</span></span> <span data-ttu-id="df2d0-125">Apenas uma única sessão física é exposta, que é uma área que começa no início do disco que representa a área endereçável inteira que tem o potencial de conter várias sessões lógicas.</span><span class="sxs-lookup"><span data-stu-id="df2d0-125">Only a single physical session is exposed, which is an area starting at the beginning of the disc representing the entire addressable area that has the potential to contain multiple logical sessions.</span></span>

> [!Note]  
> <span data-ttu-id="df2d0-126">Embora o DVD-RW seja uma exceção em que ele dá suporte ao conceito de uma sessão física no modo sequencial, atualmente esse recurso não é suportado pelo IMAPi.</span><span class="sxs-lookup"><span data-stu-id="df2d0-126">While DVD-RW is an exception in that it supports the concept of a physical session in the Sequential mode, this capability is currently not supported by IMAPI.</span></span>

 

<span data-ttu-id="df2d0-127">Para resolver a falta de um mapeamento de um para um entre sessões físicas e lógicas em formatos regraváveis, o IMAPi atualiza seletivamente as estruturas de âncora (AVDP) na *primeira* sessão lógica para apontar para as novas estruturas de volume (VDS) e as estruturas de metadados do sistema de arquivos (FSD) no início da *última* sessão lógica, conforme descrito no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="df2d0-127">To address the lack of one-to-one mapping between physical and logical sessions on rewritable formats, IMAPI selectively updates the anchor structures (AVDP) in the *first* logical session to point to the new volume structures (VDS) and file system metadata structures (FSD) at the beginning of the *last* logical session as outlined in the following diagram:</span></span>

![Diagrama que mostra a estrutura de metadados do sistema de arquivos com o "ponto de montagem da importação/F S" indicado com uma seta vermelha na "âncora" da sessão lógica 1.](images/multises2.png)

> [!Note]  
> <span data-ttu-id="df2d0-129">Esta figura ilustra o layout do disco IMAPi ao usar o UDF 2,50 com metadados redundantes.</span><span class="sxs-lookup"><span data-stu-id="df2d0-129">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="df2d0-130">Ao adicionar uma nova sessão lógica a um disco regravável, o IMAPi primeiro determina o fim da última sessão lógica analisando os metadados do volume (VDS).</span><span class="sxs-lookup"><span data-stu-id="df2d0-130">When adding a new logical session to a rewritable disc, IMAPI first determines the end of the last logical session by analyzing the volume metadata (VDS).</span></span> <span data-ttu-id="df2d0-131">Em seguida, o IMAPi adiciona a nova sessão lógica, completa com nova âncora (AVDP), volume (VDS) e estruturas de metadados do sistema de arquivos (FSD), fisicamente contígua com a sessão lógica gravada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="df2d0-131">IMAPI then adds the new logical session, complete with new anchor (AVDP), volume (VDS) and file system metadata structures (FSD), physically contiguous with the previously recorded logical session.</span></span> <span data-ttu-id="df2d0-132">A etapa final exige que as estruturas de âncora (AVDP) no início da primeira sessão lógica sejam atualizadas para apontar para as estruturas de volume (VDS) na *nova* sessão lógica.</span><span class="sxs-lookup"><span data-stu-id="df2d0-132">The final step requires that the anchor structures (AVDP) at the beginning of the first logical session are updated to point to the volume structures (VDS) in the *new* logical session.</span></span> <span data-ttu-id="df2d0-133">O resultado operacional é o mesmo que com mídia sequencial.</span><span class="sxs-lookup"><span data-stu-id="df2d0-133">The operational result is the same as with sequential media.</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="df2d0-134">Recomendações adicionais</span><span class="sxs-lookup"><span data-stu-id="df2d0-134">Additional Recommendations</span></span>

-   <span data-ttu-id="df2d0-135">**Layout de partição**</span><span class="sxs-lookup"><span data-stu-id="df2d0-135">**Partition Layout**</span></span>

    <span data-ttu-id="df2d0-136">Para obter o IMAPi compatibilidade, é recomendável que os desenvolvedores de software de gravação de terceiros usem os layouts de disco descritos nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="df2d0-136">To achieve IMAPI compatiblity, it is recommended that third-party burning software developers use the disc layouts outlined in this documentation.</span></span> <span data-ttu-id="df2d0-137">Os desenvolvedores devem evitar layouts com partições de sistema de arquivos ocupando todo o disco, pois isso requer a gravação de aplicativos para localizar espaço livre nas partições existentes sempre que os dados precisam ser anexados ao disco. Muitas vezes, os aplicativos de gravação realizam isso utilizando marcadores proprietários no disco para indicar quanto espaço está realmente ocupado pelos dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="df2d0-137">Developers should avoid layouts with file system partitions occupying the entire disc, as this requires recording applications to locate free space within existing partitions whenever data needs to be appended to the disc. Oftentimes, the recording applications accomplish this by utilizing proprietary markers on the disc to indicate how much space is actually occupied by user data.</span></span> <span data-ttu-id="df2d0-138">Esses layouts de disco são incompatíveis com o IMAPi, pois os marcadores proprietários não são reconhecidos fora do aplicativo para o qual foram criados.</span><span class="sxs-lookup"><span data-stu-id="df2d0-138">Such disc layouts are incompatible with IMAPI as the proprietary markers are not recognized outside of the application they were created for.</span></span>

-   <span data-ttu-id="df2d0-139">**Tipo de partição UDF**</span><span class="sxs-lookup"><span data-stu-id="df2d0-139">**UDF Partition Type**</span></span>

    <span data-ttu-id="df2d0-140">O IMAPi usa o tipo de partição UDF **somente leitura** em sua implementação de várias sessões na mídia regravável.</span><span class="sxs-lookup"><span data-stu-id="df2d0-140">IMAPI uses the **Read-Only** UDF partition type in its implementation of multisession on rewritable media.</span></span> <span data-ttu-id="df2d0-141">Os desenvolvedores de software de gravação de terceiros devem usar o tipo de partição UDF **somente leitura** para obter compatibilidade com a gravação mestra do Windows via IMAPI.</span><span class="sxs-lookup"><span data-stu-id="df2d0-141">Developers of third-party burning software should use the **Read-Only** UDF partition type to achieve compatiblity with Windows mastered burning via IMAPI.</span></span> <span data-ttu-id="df2d0-142">Se outro tipo de partição UDF, como **regravável** , for usado, o IMAPI não poderá fornecer suporte à masterização.</span><span class="sxs-lookup"><span data-stu-id="df2d0-142">If another UDF partition type such as **Rewritable** is used, IMAPI cannot provide mastering support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df2d0-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df2d0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df2d0-144">Criando um disco de várias sessões</span><span class="sxs-lookup"><span data-stu-id="df2d0-144">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)
</dt> <dt>

[<span data-ttu-id="df2d0-145">**IMultisessionRandomWrite**</span><span class="sxs-lookup"><span data-stu-id="df2d0-145">**IMultisessionRandomWrite**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




