---
description: Configurando a região do DVD inicial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Configurando a região do DVD inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500134"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="089f3-103">Configurando a região do DVD inicial</span><span class="sxs-lookup"><span data-stu-id="089f3-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="089f3-104">É responsabilidade do fabricante do sistema selecionar uma região de DVD inicial para a unidade de DVD em seus PCs.</span><span class="sxs-lookup"><span data-stu-id="089f3-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="089f3-105">Somente discos criptografados podem ser usados para definir a região.</span><span class="sxs-lookup"><span data-stu-id="089f3-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="089f3-106">Windows 2000 e posterior</span><span class="sxs-lookup"><span data-stu-id="089f3-106">Windows 2000 and Later</span></span>

<span data-ttu-id="089f3-107">A partir do Windows 2000, a região de DVD padrão é selecionada com base na localidade para a qual o computador está configurado.</span><span class="sxs-lookup"><span data-stu-id="089f3-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="089f3-108">O Windows 2000 sempre definirá a região inicial para uma unidade de DVD usando essa região padrão, bem como a região do disco, se houver um disco na unidade.</span><span class="sxs-lookup"><span data-stu-id="089f3-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="089f3-109">O fabricante do sistema não precisa fazer nada para definir a região inicial para as unidades de DVD do Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="089f3-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="089f3-110">Para unidades RPC1, se não houver nenhum disco na unidade durante a inicialização, a região padrão será definida com base apenas na localidade da máquina.</span><span class="sxs-lookup"><span data-stu-id="089f3-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="089f3-111">Se houver um disco de DVD na unidade durante a inicialização, a região padrão será selecionada para ser a região da unidade, desde que ela corresponda a uma região do disco; caso contrário, a região mais baixa no disco será escolhida como a região inicial da unidade.</span><span class="sxs-lookup"><span data-stu-id="089f3-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="089f3-112">O usuário (ou fabricante do sistema) tem uma alteração restante permitida, caso o padrão não esteja correto.</span><span class="sxs-lookup"><span data-stu-id="089f3-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="089f3-113">Para unidades RPC2, se durante o processo de instalação o Windows 2000 descobrir que a unidade não tem nenhuma região definida, ele tentará escolher uma região como acima, mas somente se houver um disco na unidade.</span><span class="sxs-lookup"><span data-stu-id="089f3-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="089f3-114">(As unidades RPC1 escolherão a região sem nenhum disco na unidade).</span><span class="sxs-lookup"><span data-stu-id="089f3-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="089f3-115">Depois que uma região é definida para unidades RPC2, ela não é alterada automaticamente por uma reinstalação ou por uma instalação limpa do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="089f3-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="089f3-116">O OEM pode definir uma chave do registro que contém a região do DVD padrão para o sistema.</span><span class="sxs-lookup"><span data-stu-id="089f3-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="089f3-117">Na primeira inicialização, a região da unidade será definida com esse valor.</span><span class="sxs-lookup"><span data-stu-id="089f3-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="089f3-118">A chave do registro no Windows 2000 e posterior é HKLM \\ System \\ CurrentControlSet \\ Control \\ classe \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).</span><span class="sxs-lookup"><span data-stu-id="089f3-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="089f3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="089f3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="089f3-120">Suporte à alteração da região do DVD no Windows</span><span class="sxs-lookup"><span data-stu-id="089f3-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



