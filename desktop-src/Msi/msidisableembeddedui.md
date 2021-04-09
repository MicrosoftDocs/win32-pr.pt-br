---
description: Se essa política do sistema por máquina for definida como 1, a capacidade de usar a interface do usuário inserida será desabilitada no computador. O valor padrão é 0, o que habilita o recurso de manipuladores de interface do usuário inserido.
ms.assetid: f69d69a3-3c28-4841-a334-3acb61a06bc2
title: MsiDisableEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f5bfe6abfbb386253631c2858dab6ef36bcf39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922814"
---
# <a name="msidisableembeddedui"></a><span data-ttu-id="fba45-104">MsiDisableEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="fba45-104">MsiDisableEmbeddedUI</span></span>

<span data-ttu-id="fba45-105">Se essa [política do sistema](system-policy.md) por máquina for definida como 1, a capacidade de usar a interface do usuário inserida será desabilitada no computador.</span><span class="sxs-lookup"><span data-stu-id="fba45-105">If this per-machine [system policy](system-policy.md) is set to 1, the capability to use embedded UI is disabled on the computer.</span></span> <span data-ttu-id="fba45-106">O valor padrão é 0, o que habilita o recurso de manipuladores de interface do usuário inserido.</span><span class="sxs-lookup"><span data-stu-id="fba45-106">The default value is 0, which enables the embedded UI handlers capability.</span></span>

<span data-ttu-id="fba45-107">Para desabilitar a interface do usuário inserida para um único pacote, você pode usar a propriedade [**MSIDISABLEEEUI**](msidisableeeui.md) .</span><span class="sxs-lookup"><span data-stu-id="fba45-107">To disable the embedded UI for a single package, you can use the [**MSIDISABLEEEUI**](msidisableeeui.md) property.</span></span>

<span data-ttu-id="fba45-108">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="fba45-108">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="fba45-109">Essa função está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="fba45-109">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fba45-110">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="fba45-110">Registry Key</span></span>

<span data-ttu-id="fba45-111">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="fba45-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fba45-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="fba45-112">Data Type</span></span>

<span data-ttu-id="fba45-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fba45-113">**REG\_DWORD**</span></span>

 

 



