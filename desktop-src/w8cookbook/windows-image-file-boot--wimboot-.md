---
title: Inicialização do arquivo de imagem do Windows (WimBoot)
description: Inicialização do arquivo de imagem do Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103642935"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="d36af-103">Inicialização do arquivo de imagem do Windows (WimBoot)</span><span class="sxs-lookup"><span data-stu-id="d36af-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="d36af-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d36af-104">Platform</span></span>

<span data-ttu-id="d36af-105">**Clientes:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d36af-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="d36af-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d36af-106">Description</span></span>

<span data-ttu-id="d36af-107">O WimBoot é uma maneira alternativa para os OEMs implantarem o Windows.</span><span class="sxs-lookup"><span data-stu-id="d36af-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="d36af-108">Uma implantação do WimBoot é inicializada e executa o Windows diretamente de um arquivo compactado de imagem do Windows (WIM).</span><span class="sxs-lookup"><span data-stu-id="d36af-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="d36af-109">Esse arquivo WIM é imutável e o acesso a ele é gerenciado por um novo driver de filtro do sistema de arquivos (WoF.sys).</span><span class="sxs-lookup"><span data-stu-id="d36af-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="d36af-110">O resultado é uma redução significativa no espaço em disco necessário para instalar o Windows.</span><span class="sxs-lookup"><span data-stu-id="d36af-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="d36af-111">Manifestações</span><span class="sxs-lookup"><span data-stu-id="d36af-111">Manifestations</span></span>

<span data-ttu-id="d36af-112">A maioria dos aplicativos deve ser completamente não afetada pelo WimBoot.</span><span class="sxs-lookup"><span data-stu-id="d36af-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="d36af-113">Somente os aplicativos que acessam e desbloqueiam arquivos do sistema ou arquivos pré-carregados para acesso de gravação podem ser afetados.</span><span class="sxs-lookup"><span data-stu-id="d36af-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="d36af-114">Como o WIM é imutável, as atualizações para ele (ou seja, arquivos do sistema ou pré-carregados) são simplesmente armazenadas na partição C: \\ .</span><span class="sxs-lookup"><span data-stu-id="d36af-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="d36af-115">Se um aplicativo desbloqueou o acesso de gravação para todo o sistema com suporte para WIM e arquivos pré-carregados, a economia que o WimBoot fornece será completamente perdida, pois todos esses arquivos seriam descompactados e colocados no volume C: \\ .</span><span class="sxs-lookup"><span data-stu-id="d36af-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="d36af-116">Além disso, os aplicativos de backup e restauração precisam estar cientes das implantações do WimBoot, já que o WIM está presente em uma partição separada; ou seja, em backup, as partições C: \\ e Wim devem ser salvas e ambas devem ser restauradas juntas.</span><span class="sxs-lookup"><span data-stu-id="d36af-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="d36af-117">Solução</span><span class="sxs-lookup"><span data-stu-id="d36af-117">Solution</span></span>

<span data-ttu-id="d36af-118">Foram introduzidas novas APIs que permitem que os aplicativos consultem diretamente se um determinado volume ou arquivo é apoiado por um WIM.</span><span class="sxs-lookup"><span data-stu-id="d36af-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="d36af-119">Essas informações permitem que os aplicativos tomem decisões apropriadas, como abrir esses arquivos somente para acesso de leitura ou para identificar volumes/partições que precisam ser armazenados em backup e restaurados juntos.</span><span class="sxs-lookup"><span data-stu-id="d36af-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="d36af-120">Compatibilidade, desempenho, confiabilidade ou testes de usabilidade</span><span class="sxs-lookup"><span data-stu-id="d36af-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="d36af-121">Os desenvolvedores de aplicativos devem testar seu software e seus cenários correspondentes em um sistema WimBoot, especialmente se esses aplicativos acessarem arquivos de sistema ou pré-carregados.</span><span class="sxs-lookup"><span data-stu-id="d36af-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="d36af-122">A atenção especial deve ser paga a uma redução significativa no espaço em disco disponível após a conclusão de um cenário.</span><span class="sxs-lookup"><span data-stu-id="d36af-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




