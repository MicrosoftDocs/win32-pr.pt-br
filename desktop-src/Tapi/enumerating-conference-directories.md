---
description: O fragmento de código a seguir ilustra a enumeração de conferências em um servidor ILS especificado. Este fragmento pressupõe que a conexão com um servidor ILS já foi executada.
ms.assetid: da01c534-c700-4b4f-ac22-cede9930f80d
title: Enumerando diretórios de conferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eedffb44d92f52293dc9d1add8b53588503282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461232"
---
# <a name="enumerating-conference-directories"></a><span data-ttu-id="08d2a-104">Enumerando diretórios de conferência</span><span class="sxs-lookup"><span data-stu-id="08d2a-104">Enumerating Conference Directories</span></span>

<span data-ttu-id="08d2a-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08d2a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08d2a-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="08d2a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="08d2a-107">O fragmento de código a seguir ilustra a enumeração de conferências em um servidor ILS especificado.</span><span class="sxs-lookup"><span data-stu-id="08d2a-107">The following code fragment illustrates the enumeration of conferences on a specified ILS server.</span></span> <span data-ttu-id="08d2a-108">Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada.</span><span class="sxs-lookup"><span data-stu-id="08d2a-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
SysFreeString( bNameToSearch );
```



## <a name="related-topics"></a><span data-ttu-id="08d2a-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08d2a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d2a-110">**IEnumDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="08d2a-110">**IEnumDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)
</dt> </dl>

 

 



