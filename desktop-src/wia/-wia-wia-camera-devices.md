---
description: O WIA representa um dispositivo de câmera como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de câmera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164520"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="4bb29-103">Dispositivos de câmera WIA</span><span class="sxs-lookup"><span data-stu-id="4bb29-103">WIA Camera Devices</span></span>

<span data-ttu-id="4bb29-104">O WIA representa um dispositivo de câmera como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="4bb29-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="4bb29-105">O item raiz, retornado de uma chamada para o método Gerenciador de dispositivo de aquisição de imagens do Windows (WIA) [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) , é usado para obter e definir informações do dispositivo, para controlar o dispositivo e para iniciar a enumeração do item do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bb29-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="4bb29-106">O WIA não oferece suporte a câmeras no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4bb29-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="4bb29-107">Para essas versões do Windows, use a API do dispositivo portátil do Windows (WPD) descrita no kit de desenvolvimento de driver do Windows (DDK) para adquirir imagens de câmeras.</span><span class="sxs-lookup"><span data-stu-id="4bb29-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="4bb29-108">O diagrama a seguir ilustra uma implementação de câmera de exemplo.</span><span class="sxs-lookup"><span data-stu-id="4bb29-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="4bb29-109">O item da raiz da câmera tem três itens filho, duas imagens e uma pasta.</span><span class="sxs-lookup"><span data-stu-id="4bb29-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="4bb29-110">A pasta tem dois itens filho, ambas as imagens.</span><span class="sxs-lookup"><span data-stu-id="4bb29-110">The folder has two child items, both pictures.</span></span>

![implementação de câmera de exemplo](images/wihierar.gif)

 

 



