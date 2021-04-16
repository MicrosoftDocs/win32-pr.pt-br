---
description: Alteração de região do DVD subsequente
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Alteração de região do DVD subsequente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754240"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="aae09-103">Alteração de região do DVD subsequente</span><span class="sxs-lookup"><span data-stu-id="aae09-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="aae09-104">No Windows 2000 e posterior, o navegador de DVD invoca uma página de propriedades no dispositivo da unidade de DVD-ROM no Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aae09-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="aae09-105">Essa página de propriedades também é apresentada pelo aplicativo DVDPlay.exe quando uma região precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="aae09-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="aae09-106">A interface do usuário dessa página de propriedades é muito semelhante à do DVDRgn.exe e é regional no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aae09-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="aae09-107">Para unidades RPC1, os componentes do sistema operacional Windows gerenciam as alterações de região.</span><span class="sxs-lookup"><span data-stu-id="aae09-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="aae09-108">As unidades RPC2 mantêm a configuração de região em seu próprio hardware.</span><span class="sxs-lookup"><span data-stu-id="aae09-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="aae09-109">Quando o número de alterações permitidas for esgotado em uma unidade RPC2, a unidade falhará na chamada para alterar a região e o componente de alteração de região no sistema operacional indicará que ao usuário.</span><span class="sxs-lookup"><span data-stu-id="aae09-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aae09-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aae09-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae09-111">Suporte à alteração da região do DVD no Windows</span><span class="sxs-lookup"><span data-stu-id="aae09-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



