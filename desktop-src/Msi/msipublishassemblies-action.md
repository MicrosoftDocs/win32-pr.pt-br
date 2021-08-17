---
description: A ação MsiPublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Ação MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804186"
---
# <a name="msipublishassemblies-action"></a>Ação MsiPublishAssemblies

A ação MsiPublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32. A ação consulta a [tabela MsiAssembly](msiassembly-table.md) para determinar quais assemblies têm recursos sendo anunciados ou instalados no cache de assembly global e quais assemblies têm um componente pai sendo anunciado ou instalado em um local isolado para um aplicativo específico. Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).

no Microsoft Windows XP e em sistemas posteriores, Windows Installer pode instalar assemblies [do Win32 como assemblies lado a lado](side-by-side-assemblies.md). Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação MsiPublishAssemblies deve vir após a [ação InstallInitialize](installinitialize-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md) ou na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Contexto do aplicativo.       |
| \[2\] | Nome do assembly.             |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte [assemblies](assemblies.md).

A [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gerencia o anúncio de assemblies que estão sendo removidos.

 

 
