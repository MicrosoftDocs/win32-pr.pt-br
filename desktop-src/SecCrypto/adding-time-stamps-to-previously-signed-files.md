---
description: Os carimbos de data e hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a opção-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Adicionando carimbos de data/hora a arquivos assinados anteriormente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105756380"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="1be38-103">Adicionando carimbos de data/hora a arquivos assinados anteriormente</span><span class="sxs-lookup"><span data-stu-id="1be38-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="1be38-104">Os carimbos de data e hora normalmente são incluídos quando um arquivo é assinado usando SignTool com a opção **-t** .</span><span class="sxs-lookup"><span data-stu-id="1be38-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="1be38-105">Além disso, carimbos de data/hora podem ser adicionados a arquivos que foram assinados sem um carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="1be38-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="1be38-106">O comando a seguir adiciona um carimbo de data/hora a um arquivo assinado anteriormente:</span><span class="sxs-lookup"><span data-stu-id="1be38-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="1be38-107">**carimbo de data/hora de SignTool-t https: \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="1be38-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="1be38-108">O carimbo de data/hora do arquivo deve ter sido assinado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1be38-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="1be38-109">Para obter mais informações sobre SignTool, consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="1be38-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



