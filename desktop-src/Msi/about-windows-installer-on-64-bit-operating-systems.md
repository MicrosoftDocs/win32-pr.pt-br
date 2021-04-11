---
description: Windows Installer é executado como um serviço em computadores usando o Windows de 32 bits ou 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Sobre Windows Installer em sistemas operacionais de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "104172353"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="278f4-103">Sobre Windows Installer em sistemas operacionais de 64 bits</span><span class="sxs-lookup"><span data-stu-id="278f4-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="278f4-104">Windows Installer é executado como um serviço em computadores usando o Windows de 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="278f4-105">As versões do instalador anteriores à versão 2,0 podem instalar e gerenciar pacotes de Windows Installer de 32 bits somente em sistemas operacionais de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="278f4-106">Observe que você não pode anunciar ou instalar um aplicativo de 64 bits em um sistema operacional de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="278f4-107">Um pacote de Windows Installer deve ser especificado como um pacote de 32 bits ou de 64 bits; Ele não pode ser especificado como neutro.</span><span class="sxs-lookup"><span data-stu-id="278f4-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="278f4-108">Em um computador que usa um sistema operacional de 64 bits, o serviço de Windows Installer é hospedado em um processo de 64 bits que instala pacotes de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="278f4-109">Windows Installer instala três tipos de pacotes do Windows Installer em um computador que executa um sistema operacional de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="278f4-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="278f4-110">pacotes de 32 bits que contêm apenas componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="278f4-111">pacotes de 64 bits contendo alguns componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="278f4-112">pacotes de 64 bits contendo apenas componentes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="278f4-113">As seções a seguir descrevem os dois tipos de pacotes de Windows Installer e as novas propriedades do instalador fornecidas pelo Windows Installer para pacotes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="278f4-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="278f4-114">Pacotes de Windows Installer de 32 bits</span><span class="sxs-lookup"><span data-stu-id="278f4-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="278f4-115">Pacotes de Windows Installer de 64 bits</span><span class="sxs-lookup"><span data-stu-id="278f4-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="278f4-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="278f4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278f4-117">Usando pacotes de Windows Installer de 64 bits</span><span class="sxs-lookup"><span data-stu-id="278f4-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



