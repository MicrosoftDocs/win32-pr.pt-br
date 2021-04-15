---
description: Se essa política do sistema por máquina estiver definida como 1, nenhum pacote no sistema obterá a funcionalidade de componente compartilhado habilitada pelo atributo msidbComponentAttributesShared na tabela de componentes.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501984"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="d97f3-103">DisableSharedComponent</span><span class="sxs-lookup"><span data-stu-id="d97f3-103">DisableSharedComponent</span></span>

<span data-ttu-id="d97f3-104">Se essa [política do sistema](system-policy.md) por máquina estiver definida como 1, nenhum pacote no sistema obterá a funcionalidade de componente compartilhado habilitada pelo atributo **msidbComponentAttributesShared** na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d97f3-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="d97f3-105">O valor padrão é 0, que habilita a funcionalidade do componente compartilhado para componentes marcados com **msidbComponentAttributesShared** em todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="d97f3-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="d97f3-106">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="d97f3-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="d97f3-107">Essa função está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="d97f3-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="d97f3-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="d97f3-108">Registry Key</span></span>

<span data-ttu-id="d97f3-109">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d97f3-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d97f3-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d97f3-110">Data Type</span></span>

<span data-ttu-id="d97f3-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d97f3-111">**REG\_DWORD**</span></span>

 

 



