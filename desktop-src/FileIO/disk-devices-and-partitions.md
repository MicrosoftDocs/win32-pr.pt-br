---
description: Descreve um disco rígido, particionamento e o registro mestre de inicialização.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Partições e dispositivos de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557046"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="4e971-103">Partições e dispositivos de disco</span><span class="sxs-lookup"><span data-stu-id="4e971-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="4e971-104">Um disco rígido consiste em um conjunto de platters empilhados, cada um dos quais tem dados armazenados de forma eletromagnética em círculos concêntricos ou *faixas*.</span><span class="sxs-lookup"><span data-stu-id="4e971-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="4e971-105">Cada platter tem dois cabeçotes, um em cada lado do platter, que lê ou grava dados conforme o disco gira.</span><span class="sxs-lookup"><span data-stu-id="4e971-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="4e971-106">Uma *unidade de disco rígido* controla o posicionamento, a leitura e a gravação do disco rígido.</span><span class="sxs-lookup"><span data-stu-id="4e971-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="4e971-107">Observe que os cabeçotes de todos os Platters são posicionados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="4e971-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="4e971-108">A menor unidade endereçável de uma faixa é um *setor*.</span><span class="sxs-lookup"><span data-stu-id="4e971-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="4e971-109">Um *cilindro* é definido como o conjunto de faixas que aparecem no mesmo local em cada platter.</span><span class="sxs-lookup"><span data-stu-id="4e971-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="4e971-110">Por exemplo, o diagrama a seguir mostra um disco rígido com quatro Platters.</span><span class="sxs-lookup"><span data-stu-id="4e971-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="4e971-111">O cilindro X consiste em oito trilhas (Track X de cada lado de cada platter).</span><span class="sxs-lookup"><span data-stu-id="4e971-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![disco rígido, incluindo faixas, setores e platters](images/diskdevice.png)

<span data-ttu-id="4e971-113">Um disco rígido pode conter uma ou mais regiões lógicas chamadas *partições*.</span><span class="sxs-lookup"><span data-stu-id="4e971-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="4e971-114">As partições são criadas quando o usuário formata um disco rígido como um *disco básico*.</span><span class="sxs-lookup"><span data-stu-id="4e971-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="4e971-115">O Windows também dá suporte a *discos dinâmicos*, que não são discutidos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="4e971-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="4e971-116">Para obter mais informações sobre discos básicos e discos dinâmicos, consulte [discos básicos e dinâmicos](basic-and-dynamic-disks.md).</span><span class="sxs-lookup"><span data-stu-id="4e971-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="4e971-117">A criação de várias partições em um disco permite a aparência de discos rígidos separados.</span><span class="sxs-lookup"><span data-stu-id="4e971-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="4e971-118">Por exemplo, um sistema com um disco rígido que tem uma partição contém um único volume, designado pelo sistema como a unidade C. Um sistema com um disco rígido com duas partições normalmente contém as unidades C e D. Ter várias partições em um disco rígido pode facilitar o gerenciamento do sistema, por exemplo, para organizar arquivos ou dar suporte a vários usuários.</span><span class="sxs-lookup"><span data-stu-id="4e971-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="4e971-119">O primeiro setor físico em um disco básico contém uma estrutura de dados conhecida como MBR (registro mestre de inicialização).</span><span class="sxs-lookup"><span data-stu-id="4e971-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="4e971-120">O MBR contém o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4e971-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="4e971-121">Um programa de inicialização (até 442 bytes de tamanho)</span><span class="sxs-lookup"><span data-stu-id="4e971-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="4e971-122">Uma assinatura de disco (um número exclusivo de 4 bytes)</span><span class="sxs-lookup"><span data-stu-id="4e971-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="4e971-123">Uma tabela de partição (até quatro entradas)</span><span class="sxs-lookup"><span data-stu-id="4e971-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="4e971-124">Um marcador de fim de MBR (sempre 0x55AA)</span><span class="sxs-lookup"><span data-stu-id="4e971-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e971-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e971-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e971-126">Sobre o gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="4e971-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="4e971-127">Discos básicos e dinâmicos</span><span class="sxs-lookup"><span data-stu-id="4e971-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



