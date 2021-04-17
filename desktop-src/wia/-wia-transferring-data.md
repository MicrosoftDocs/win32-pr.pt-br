---
description: 'Saiba mais sobre: transferindo dados'
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: Transferindo dados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763484"
---
# <a name="transferring-data"></a><span data-ttu-id="5ba81-103">Transferindo dados</span><span class="sxs-lookup"><span data-stu-id="5ba81-103">Transferring Data</span></span>

> [!Note]  
> <span data-ttu-id="5ba81-104">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="5ba81-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="5ba81-105">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="5ba81-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="5ba81-106">Use o método de [**transferência**](-wia-iwiadispatchitem-transfer.md) de um objeto [**Item**](-wia-item.md) para transferir dados de imagem ou de áudio de um dispositivo para um arquivo ou para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5ba81-106">Use the [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of an [**Item**](-wia-item.md) object to transfer image or audio data from a device to a file or the clipboard.</span></span>

<span data-ttu-id="5ba81-107">Passe um caminho e um nome de arquivo como o primeiro parâmetro para salvar os dados no disco ou passe a cadeia de caracteres "Clipboard" para transferir o item para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5ba81-107">Pass a path and filename as the first parameter to save the data to disk, or pass the string "clipboard" to transfer the item to the clipboard.</span></span>

 

 
