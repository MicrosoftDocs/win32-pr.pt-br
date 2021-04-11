---
description: Ao instalar um assembly em um local isolado para um aplicativo específico, o aplicativo deve ser especificado na \_ coluna aplicativo de arquivo da tabela MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Instalando e removendo assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172027"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="731ac-103">Instalando e removendo assemblies</span><span class="sxs-lookup"><span data-stu-id="731ac-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="731ac-104">Ao instalar um assembly em um local isolado para um aplicativo específico, o aplicativo deve ser especificado na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="731ac-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="731ac-105">Esse campo é uma chave para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="731ac-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="731ac-106">O instalador usa a estrutura de diretório especificada na tabela de [diretórios](directory-table.md) para instalar o assembly no mesmo diretório que o componente que contém esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="731ac-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="731ac-107">Ao instalar um assembly no cache de assembly global, o valor na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md) deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="731ac-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="731ac-108">As seções a seguir descrevem a instalação de assemblies do Win32 e do Common Language Runtime:</span><span class="sxs-lookup"><span data-stu-id="731ac-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="731ac-109">Instalação de assemblies Win32</span><span class="sxs-lookup"><span data-stu-id="731ac-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="731ac-110">Instalação de assemblies do Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="731ac-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



