---
description: O formato de disco rígido virtual (VHD) é uma especificação de formato de imagem disponível publicamente que permite o encapsulamento do disco rígido em um arquivo individual para uso pelo sistema operacional como um disco virtual de todas as mesmas maneiras que discos rígidos físicos são usados.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Sobre o VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647155"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span data-ttu-id="7bc5f-103"><span id="vhd.about_vhd"></span>Sobre o VHD</span><span class="sxs-lookup"><span data-stu-id="7bc5f-103"><span id="vhd.about_vhd"></span>About VHD</span></span>

<span data-ttu-id="7bc5f-104">O formato de disco rígido virtual (VHD) é uma [especificação](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) de formato de imagem disponível publicamente que permite o encapsulamento do disco rígido em um arquivo individual para uso pelo sistema operacional como um *disco virtual* de todas as mesmas maneiras que discos rígidos físicos são usados.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-104">The Virtual Hard Disk (VHD) format is a publicly-available image format [specification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) that allows encapsulation of the hard disk into an individual file for use by the operating system as a *virtual disk* in all the same ways physical hard disks are used.</span></span> <span data-ttu-id="7bc5f-105">Esses discos virtuais são capazes de hospedar sistemas de arquivos nativos (NTFS, FAT, exFAT e UDFS) enquanto dão suporte a operações de arquivo e disco padrão.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-105">These virtual disks are capable of hosting native file systems (NTFS, FAT, exFAT, and UDFS) while supporting standard disk and file operations.</span></span> <span data-ttu-id="7bc5f-106">O suporte à API do VHD permite o gerenciamento dos discos virtuais.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-106">VHD API support allows management of the virtual disks.</span></span> <span data-ttu-id="7bc5f-107">Os discos virtuais criados com a API VHD podem funcionar como discos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-107">Virtual disks created with the VHD API can function as boot disks.</span></span>

<span data-ttu-id="7bc5f-108">Um exemplo de como os arquivos VHD são usados é o recurso do [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) no Windows 7, no windows Server 2008, no Virtual Server e no Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-108">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows 7, Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="7bc5f-109">Esses produtos usam a API do VHD para conter a imagem do sistema operacional Windows utilizada por uma máquina virtual como seu disco de inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-109">These products use the VHD API to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

<span data-ttu-id="7bc5f-110">O SDK (Software Development Kit) do Microsoft Windows integra o suporte nativo do VHD para trabalhar com discos virtuais, facilitando para os desenvolvedores e administradores criar, gerenciar e implantar imagens do Windows em arquivos VHD usando o suporte à API de plataforma ou as ferramentas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with virtual disks, making it easier for developers and administrators to create, manage, and deploy Windows images in VHD files using either the platform API support or management tools.</span></span> <span data-ttu-id="7bc5f-111">Não é necessário instalar aplicativos separados ou implementar um analisador de formato VHD para habilitar essas operações.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="7bc5f-112">Essas APIs permitem o uso genérico de discos virtuais independentemente de outras tecnologias de virtualização.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-112">These APIs allow for generic use of virtual disks independent of any other virtualization technologies.</span></span>

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span data-ttu-id="7bc5f-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologia</span><span class="sxs-lookup"><span data-stu-id="7bc5f-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminology</span></span>

<span data-ttu-id="7bc5f-114">O termo *repositório de backup* é usado para fazer referência ao arquivo físico que existe no disco rígido real.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-114">The term *backing store* is used to refer to the physical file that exists on the actual hard disk.</span></span> <span data-ttu-id="7bc5f-115">O repositório de backup é representado por um *arquivo de imagem VHD*.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-115">The backing store is represented by a *VHD image file*.</span></span>

<span data-ttu-id="7bc5f-116">Os termos *dinâmicos*, *expansíveis* e *esparsos* costumam ser usados de maneira intercambiável ao se referir a discos virtuais expansíveis dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-116">The terms *dynamic*, *expandable*, and *sparse* are often used interchangeably when referring to dynamically expandable virtual disks.</span></span> <span data-ttu-id="7bc5f-117">Para a tecnologia VHD, esses termos são idênticos.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-117">For VHD technology, these terms are identical.</span></span>

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span data-ttu-id="7bc5f-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Visão geral dos recursos do sistema VHD</span><span class="sxs-lookup"><span data-stu-id="7bc5f-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD System Features Overview</span></span>

<span data-ttu-id="7bc5f-119">O diagrama a seguir apresenta uma visão geral dos recursos do VHD e suas relações.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-119">The following diagram presents an overview of the VHD features and their relationships.</span></span>

![diagrama de bloco VHD](images/vhd.png)

<span data-ttu-id="7bc5f-121">Veja a seguir uma explicação resumida dos recursos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-121">The following is a summary explanation of the previously described features.</span></span>

<span data-ttu-id="7bc5f-122">APIs nativas do Windows no modo de usuário:</span><span class="sxs-lookup"><span data-stu-id="7bc5f-122">User Mode Native Windows APIs:</span></span>

-   <span data-ttu-id="7bc5f-123">VirtDisk.dll-biblioteca comum para APIs de gerenciamento de VHD.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-123">VirtDisk.dll - Common library for VHD management APIs.</span></span>

<span data-ttu-id="7bc5f-124">Wrappers de gerenciamento específicos de domínio do modo de usuário:</span><span class="sxs-lookup"><span data-stu-id="7bc5f-124">User Mode Domain-specific Management Wrappers:</span></span>

-   <span data-ttu-id="7bc5f-125">[APIs VHD do VDS](/windows/desktop/VDS/about-vds) – wrappers do modelo de objeto VDS para as APIs do Windows VHD.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-125">[VDS VHD APIs](/windows/desktop/VDS/about-vds) - VDS Object Model wrappers for the VHD Windows APIs.</span></span>

<span data-ttu-id="7bc5f-126">Drivers de modo kernel:</span><span class="sxs-lookup"><span data-stu-id="7bc5f-126">Kernel Mode Drivers:</span></span>

-   <span data-ttu-id="7bc5f-127">Enumerador de unidade virtual de VDrvRoot.sys raiz.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-127">VDrvRoot.sys - Root virtual drive enumerator.</span></span>
-   <span data-ttu-id="7bc5f-128">Gerenciamento de dependência de volume aninhado por FsDepends.sys.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-128">FsDepends.sys - Nested volume dependency management.</span></span>
-   <span data-ttu-id="7bc5f-129">Vhdmp.sys-analisador de VHD e provedor de propriedade de dependência.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-129">Vhdmp.sys - VHD parser and dependency property provider.</span></span>

<span data-ttu-id="7bc5f-130">A documentação do SDK nesta seção aborda as APIs VHD do Windows nativas do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-130">The SDK documentation in this section covers the user-mode native Windows VHD APIs.</span></span>

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span data-ttu-id="7bc5f-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipos de disco virtual</span><span class="sxs-lookup"><span data-stu-id="7bc5f-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtual Disk Types</span></span>

<span data-ttu-id="7bc5f-132">Há considerações para usar discos virtuais e quais tipos de discos virtuais estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="7bc5f-132">There are considerations for using virtual disks, and what types of virtual disks are available:</span></span>

-   <span data-ttu-id="7bc5f-133">**Corrigido**– o arquivo de imagem VHD é previamente alocado no repositório de backup para o tamanho máximo solicitado.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-133">**Fixed**—The VHD image file is pre-allocated on the backing store for the maximum size requested.</span></span>
-   <span data-ttu-id="7bc5f-134">**Expansível**– também conhecido como "dinâmico", "expansível dinamicamente" e "esparso", o arquivo de imagem VHD usa apenas o espaço no armazenamento de backup, conforme necessário, para armazenar os dados reais que o disco virtual contém atualmente.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-134">**Expandable**—Also known as "dynamic", "dynamically expandable", and "sparse", the VHD image file uses only as much space on the backing store as needed to store the actual data the virtual disk currently contains.</span></span> <span data-ttu-id="7bc5f-135">Ao criar esse tipo de disco virtual, a API VHD não testa o espaço livre no disco físico com base no tamanho máximo solicitado, portanto, é possível criar com êxito um disco virtual dinâmico com um tamanho máximo maior do que o espaço livre disponível no disco físico.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-135">When creating this type of virtual disk, the VHD API does not test for free space on the physical disk based on the maximum size requested, therefore it is possible to successfully create a dynamic virtual disk with a maximum size larger than the available physical disk free space.</span></span> <span data-ttu-id="7bc5f-136">Para obter mais informações, consulte [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="7bc5f-136">For more information, see [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span></span>
    <span data-ttu-id="7bc5f-137">**Observação**  O tamanho máximo de um disco virtual dinâmico é de 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-137">**Note**  The maximum size of a dynamic virtual disk is 2,040 GB.</span></span>

     

-   <span data-ttu-id="7bc5f-138">**Diferenciação**— um disco virtual pai é usado como base desse tipo, com quaisquer gravações subsequentes gravadas no disco virtual como diferenças no novo arquivo de imagem VHD diferencial e o arquivo de imagem VHD pai não é modificado.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-138">**Differencing**—A parent virtual disk is used as the basis of this type, with any subsequent writes written to the virtual disk as differences to the new differencing VHD image file, and the parent VHD image file is not modified.</span></span> <span data-ttu-id="7bc5f-139">Por exemplo, se você tiver um disco virtual do sistema operacional de inicialização do sistema de instalação limpa como pai e designar o disco virtual diferencial como o disco virtual atual para o sistema usar, o sistema operacional no disco virtual pai permanecerá em seu estado original para recuperação rápida ou para criar rapidamente mais imagens de inicialização com base em discos virtuais diferenciais adicionais.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-139">For example, if you have a clean-install system boot operating system virtual disk as a parent and designate the differencing virtual disk as the current virtual disk for the system to use, then the operating system on the parent virtual disk stays in its original state for quick recovery or for quickly creating more boot images based on additional differencing virtual disks.</span></span> <span data-ttu-id="7bc5f-140">Para obter mais informações, consulte [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="7bc5f-140">For more information, see [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span></span>
    <span data-ttu-id="7bc5f-141">**Observação**  O tamanho máximo de um disco virtual diferencial é de 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-141">**Note**  The maximum size of a differencing virtual disk is 2,040 GB.</span></span>

     

<span data-ttu-id="7bc5f-142">Todos os tipos de disco virtual têm um tamanho mínimo de 3 MB.</span><span class="sxs-lookup"><span data-stu-id="7bc5f-142">All virtual disk types have a minimum size of 3 MB.</span></span>

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="7bc5f-143"><span id="related_topics"></span>Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc5f-143"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="7bc5f-144">Sobre o VDS</span><span class="sxs-lookup"><span data-stu-id="7bc5f-144">About VDS</span></span>](/windows/desktop/VDS/about-vds)

[<span data-ttu-id="7bc5f-145">Referência do VHD</span><span class="sxs-lookup"><span data-stu-id="7bc5f-145">VHD Reference</span></span>](vhd-reference.md)

[<span data-ttu-id="7bc5f-146">Especificação de formato de imagem de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="7bc5f-146">Virtual Hard Disk Image Format Specification</span></span>](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
