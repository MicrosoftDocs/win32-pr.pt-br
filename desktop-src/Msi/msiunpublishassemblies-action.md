---
description: A ação MsiUnpublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo removidos.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Ação MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829564"
---
# <a name="msiunpublishassemblies-action"></a>Ação MsiUnpublishAssemblies

A ação MsiUnpublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo removidos. A ação consulta a [tabela MsiAssembly](msiassembly-table.md) para determinar quais assemblies têm recursos anunciados ou instalados que estão sendo removidos do cache de assembly global e quais assemblies têm um componente pai anunciado ou instalado que está sendo removido de um local isolado para um aplicativo específico. Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).

Em sistemas que executam o Windows XP e versões posteriores, Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md). Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação MsiUnpublishAssemblies deve vir após a [ação InstallInitialize](installinitialize-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Contexto do aplicativo.       |
| \[2\] | Nome do assembly.             |



 

## <a name="remarks"></a>Comentários

A [ação MsiPublishAssemblies](msipublishassemblies-action.md) gerencia o anúncio de assemblies sendo anunciados ou instalados.

 

 
