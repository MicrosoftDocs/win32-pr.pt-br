---
description: Encapsular o disco rígido em um único arquivo para uso pelo sistema operacional como um disco virtual. Os discos virtuais podem funcionar como discos de inicialização e podem hospedar sistemas de arquivos nativos (NTFS, FAT, exFAT e UDFS) enquanto dão suporte a operações de arquivo e disco padrão.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164489"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="bba9e-104"><span id="vhd.portal"></span>Disco Virtual</span><span class="sxs-lookup"><span data-stu-id="bba9e-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="bba9e-105"><span id="purpose"></span>Objetivo</span><span class="sxs-lookup"><span data-stu-id="bba9e-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="bba9e-106">O formato VHD (disco rígido virtual) é uma especificação de formato de imagem disponível publicamente que especifica um disco rígido virtual encapsulado em um único arquivo, capaz de hospedar sistemas de arquivos nativos enquanto dá suporte a operações de disco e arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="bba9e-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="bba9e-107">Um exemplo de como os arquivos VHD são usados é o recurso do [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) no windows Server 2008, no Virtual Server e no Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="bba9e-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="bba9e-108">Esses produtos usam VHDs para conter a imagem do sistema operacional Windows utilizada por uma máquina virtual como seu disco de inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="bba9e-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="bba9e-109"><span id="developer_audience_heading"></span>Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="bba9e-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="bba9e-110">O SDK (Software Development Kit) do Microsoft Windows integra o suporte nativo do VHD para trabalhar com VHDs, facilitando para os desenvolvedores e administradores a criação, o gerenciamento e a implantação de imagens do Windows em VHDs usando o suporte à API de plataforma ou as ferramentas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bba9e-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="bba9e-111">Não é necessário instalar aplicativos separados ou implementar um analisador de formato VHD para habilitar essas operações.</span><span class="sxs-lookup"><span data-stu-id="bba9e-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="bba9e-112">Essas APIs permitem o uso genérico de VHDs independentemente de qualquer outra tecnologia de virtualização.</span><span class="sxs-lookup"><span data-stu-id="bba9e-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="bba9e-113"><span id="run_time_requirements_heading"></span>Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="bba9e-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="bba9e-114">O VHD tem suporte no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="bba9e-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="bba9e-115"><span id="in_this_section"></span>Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bba9e-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bba9e-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="bba9e-116">Topic</span></span></th>
<th><span data-ttu-id="bba9e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba9e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bba9e-118"><a href="about-vhd.md">Sobre o VHD</a></span><span class="sxs-lookup"><span data-stu-id="bba9e-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="bba9e-119">Descreve o formato VHD com dicas e sugestões de uso de API.</span><span class="sxs-lookup"><span data-stu-id="bba9e-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bba9e-120"><a href="vhd-reference.md">Referência do VHD</a></span><span class="sxs-lookup"><span data-stu-id="bba9e-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="bba9e-121">Descreve as funções, estruturas e enumerações da API do VHD.</span><span class="sxs-lookup"><span data-stu-id="bba9e-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="bba9e-122"><span id="related_topics"></span>Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bba9e-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="bba9e-123">Serviço de Disco Virtual</span><span class="sxs-lookup"><span data-stu-id="bba9e-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
