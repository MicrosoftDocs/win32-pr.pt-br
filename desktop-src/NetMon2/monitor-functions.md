---
description: Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funções de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827257"
---
# <a name="monitor-functions"></a><span data-ttu-id="a1a5a-103">Funções de monitor</span><span class="sxs-lookup"><span data-stu-id="a1a5a-103">Monitor Functions</span></span>

<span data-ttu-id="a1a5a-104">Esta seção descreve as funções auxiliares que você pode usar para desenvolver monitores personalizados.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="a1a5a-105">Função</span><span class="sxs-lookup"><span data-stu-id="a1a5a-105">Function</span></span>                                       | <span data-ttu-id="a1a5a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1a5a-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1a5a-107">DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="a1a5a-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="a1a5a-108">Cria uma instância do monitor.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="a1a5a-109">HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="a1a5a-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="a1a5a-110">Converte uma \_ cadeia de caracteres de versão HTML CP UTF8 em Unicode.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="a1a5a-111">Loaddword</span><span class="sxs-lookup"><span data-stu-id="a1a5a-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="a1a5a-112">Carrega um **DWORD** de uma cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="a1a5a-113">Loadipaddresss</span><span class="sxs-lookup"><span data-stu-id="a1a5a-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="a1a5a-114">Carrega uma lista de endereços IP de uma cadeia de caracteres de configuração de TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="a1a5a-115">LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="a1a5a-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="a1a5a-116">Carrega uma lista de endereços IPX de uma cadeia de caracteres de configuração de TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="a1a5a-117">LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="a1a5a-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="a1a5a-118">Carrega uma lista de endereços MAC de uma cadeia de caracteres de configuração de TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="a1a5a-119">LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="a1a5a-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="a1a5a-120">Transforma uma cadeia de caracteres (como "157.54.32.45") em um endereço **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a1a5a-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="a1a5a-121">LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="a1a5a-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="a1a5a-122">Procura um nome de variável solicitado na cadeia de caracteres de configuração e aloca espaço suficiente (usando **HeapAllocMemory**) para armazená-lo, copiá-lo e retorná-lo.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="a1a5a-123">OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="a1a5a-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="a1a5a-124">Indica que a DLL começou a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="a1a5a-125">O MCSVC chama essa função quando carrega pela primeira vez a DLL do monitor.</span><span class="sxs-lookup"><span data-stu-id="a1a5a-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



