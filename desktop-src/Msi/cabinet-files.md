---
description: Um gabinete é um arquivo único, geralmente com uma extensão. cab, que armazena arquivos compactados em uma biblioteca de arquivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Arquivos de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755089"
---
# <a name="cabinet-files"></a><span data-ttu-id="e8d2e-103">Arquivos de gabinete</span><span class="sxs-lookup"><span data-stu-id="e8d2e-103">Cabinet Files</span></span>

<span data-ttu-id="e8d2e-104">Um gabinete é um arquivo único, geralmente com uma extensão. cab, que armazena arquivos compactados em uma biblioteca de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="e8d2e-105">O formato de gabinete é uma maneira eficiente de empacotar vários arquivos, pois a compactação é executada em limites de arquivos, o que melhora significativamente a taxa de compactação.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="e8d2e-106">Os desenvolvedores podem usar uma ferramenta de criação de arquivo de gabinete, como Makecab.exe para criar arquivos de gabinete para uso com pacotes do instalador.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="e8d2e-107">O utilitário Makecab.exe está incluído nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e8d2e-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="e8d2e-108">Os desenvolvedores também podem usar uma ferramenta de criação de arquivo de gabinete, como Cabarc.exe para criar arquivos de gabinete para uso com pacotes do instalador.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="e8d2e-109">Essa ferramenta grava na estrutura de gabinete Diamond.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="e8d2e-110">As chaves de arquivo dos arquivos armazenados dentro de um arquivo de gabinete devem corresponder às entradas na coluna arquivo da [tabela de arquivos](file-table.md) e a sequência de arquivos no gabinete deve corresponder à sequência de arquivos especificada na coluna sequência.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="e8d2e-111">Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="e8d2e-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="e8d2e-112">Arquivos grandes podem ser divididos entre dois ou mais arquivos de gabinete.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="e8d2e-113">Não pode haver mais de 15 arquivos em um arquivo de gabinete que abranja o próximo arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="e8d2e-114">Por exemplo, se você tiver três arquivos de gabinete, o primeiro gabinete poderá ter 15 arquivos que se estendem ao segundo arquivo de gabinete e o segundo arquivo de gabinete pode ter 15 arquivos que abrangem o terceiro arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="e8d2e-115">O instalador extrai arquivos de um gabinete conforme eles são necessários para a instalação e os instala na mesma ordem em que são armazenados no arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="e8d2e-116">Os requisitos de espaço para a instalação de um arquivo armazenado em um gabinete não são diferentes de instalar um arquivo descompactado.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="e8d2e-117">Um arquivo de gabinete pode ser localizado dentro ou fora do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="e8d2e-118">A partir do Windows Installer 5,0 em execução no Windows 7 ou no Windows Server 2008 R2, o instalador salva todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="e8d2e-119">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Para conservar o espaço em disco, o instalador sempre remove todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8d2e-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



