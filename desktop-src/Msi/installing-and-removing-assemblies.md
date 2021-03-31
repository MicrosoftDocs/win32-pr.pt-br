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
# <a name="installing-and-removing-assemblies"></a>Instalando e removendo assemblies

Ao instalar um assembly em um local isolado para um aplicativo específico, o aplicativo deve ser especificado na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md). Esse campo é uma chave para a [tabela de arquivos](file-table.md). O instalador usa a estrutura de diretório especificada na tabela de [diretórios](directory-table.md) para instalar o assembly no mesmo diretório que o componente que contém esse arquivo.

Ao instalar um assembly no cache de assembly global, o valor na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md) deve ser nulo.

As seções a seguir descrevem a instalação de assemblies do Win32 e do Common Language Runtime:

-   [Instalação de assemblies Win32](installation-of-win32-assemblies.md)
-   [Instalação de assemblies do Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



