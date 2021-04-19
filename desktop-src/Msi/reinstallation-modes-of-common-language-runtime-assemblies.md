---
description: Os assemblies do Common Language Runtime instalados no cache de assembly global devem ter arquivos idênticos em todas as ocorrências do assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modos de reinstalação de assemblies do Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768463"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Modos de reinstalação de assemblies do Common Language Runtime

Os assemblies do Common Language Runtime instalados no cache de assembly global devem ter arquivos idênticos em todas as ocorrências do assembly. Isso significa que os modos de reinstalação usados por [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) e [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) devem ter significados diferentes para componentes regulares e Common Language Runtime assemblies. As definições a seguir dos modos de reinstalação se aplicam a assemblies Common Language Runtime.



| Modo de reinstalação                  | Significado para componentes de Microsoft .NET                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| reinstalação de \_ filemission      | Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.                                         |
| reinstalar o \_ FILEOLDERVERSION | Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.                                         |
| reinstalar o \_ FILEEQUALVERSION | Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.                                         |
| reinstalar o \_ FILEexato        | Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou incompleto.                                         |
| reinstalar o \_ FILEverify       | Instale ou reinstale o componente Common Language Runtime se ele estiver ausente ou se o componente existente estiver incompleto ou corrompido. |
| reinstalar o \_ FILEreplace      | Sempre instale ou reinstale o componente Common Language Runtime.                                                                 |



 

 

 



