---
description: O WIA fornece uma camada de compatibilidade TWAIN que permite que aplicativos com reconhecimento de TWAIN se comuniquem com dispositivos WIA (aquisição de imagens do Windows).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidade com TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760998"
---
# <a name="twain-compatibility"></a><span data-ttu-id="544b2-103">Compatibilidade com TWAIN</span><span class="sxs-lookup"><span data-stu-id="544b2-103">TWAIN Compatibility</span></span>

<span data-ttu-id="544b2-104">O WIA fornece uma camada de compatibilidade TWAIN que permite que aplicativos com reconhecimento de TWAIN se comuniquem com dispositivos WIA (aquisição de imagens do Windows).</span><span class="sxs-lookup"><span data-stu-id="544b2-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="544b2-105">Os aplicativos com reconhecimento de TWAIN não têm acesso completo à funcionalidade WIA.</span><span class="sxs-lookup"><span data-stu-id="544b2-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="544b2-106">Por exemplo, um aplicativo não pode suprimir a interface do usuário usando a camada de compatibilidade TWAIN.</span><span class="sxs-lookup"><span data-stu-id="544b2-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="544b2-107">Os dispositivos WIA aparecem duas vezes para um aplicativo que reconhece o WIA e o TWAIN: uma vez por meio da comunicação de WIA normal e uma vez por meio da camada de compatibilidade TWAIN.</span><span class="sxs-lookup"><span data-stu-id="544b2-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="544b2-108">Para evitar a listagem de um dispositivo WIA duas vezes, um aplicativo que reconhece o WIA e o TWAIN deve filtrar os dispositivos WIA que vêm pela camada de compatibilidade TWAIN.</span><span class="sxs-lookup"><span data-stu-id="544b2-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="544b2-109">Todos os dispositivos WIA que vêm pela camada de compatibilidade TWAIN têm "WIA-" como um prefixo, portanto, é fácil filtrá-los.</span><span class="sxs-lookup"><span data-stu-id="544b2-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



