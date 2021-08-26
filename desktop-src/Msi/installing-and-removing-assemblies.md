---
description: Ao instalar um assembly em um local isolado para um aplicativo específico, o aplicativo deve ser especificado na \_ coluna aplicativo de arquivo da tabela MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Instalando e removendo assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043426"
---
# <a name="installing-and-removing-assemblies"></a>Instalando e removendo assemblies

Ao instalar um assembly em um local isolado para um aplicativo específico, o aplicativo deve ser especificado na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md). Esse campo é uma chave para a [tabela de arquivos](file-table.md). O instalador usa a estrutura de diretório especificada na tabela de [diretórios](directory-table.md) para instalar o assembly no mesmo diretório que o componente que contém esse arquivo.

Ao instalar um assembly no cache de assembly global, o valor na \_ coluna aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md) deve ser nulo.

As seções a seguir descrevem a instalação de assemblies do Win32 e do Common Language Runtime:

-   [Instalação de assemblies Win32](installation-of-win32-assemblies.md)
-   [Instalação de assemblies do Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



