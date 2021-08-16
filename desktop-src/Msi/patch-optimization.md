---
description: Windows O instalador pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches a aplicativos instalados.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Otimização de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee37ba48764f6249410a6dfc2512245aa6ca6dfca68cff09ec15e06a42f9156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627639"
---
# <a name="patch-optimization"></a>Otimização de patch

Windows O instalador pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches a aplicativos instalados.

**Windows Instalador 2.0:** Sem suporte. Para versões do Windows Instalador lançadas antes do Windows Installer 3.0, a aplicação de patch executa uma instalação de reparo completa do aplicativo, o que pode levar muito mais tempo.

**Windows Instalador 3.0 e posterior:** O processo de aplicação de patch altera apenas as partes de um aplicativo que são modificadas por um patch.

**Windows Instalador 3.1 e posterior:** A partir do Windows 3.1, a otimização de patch requer que todos os patches na transação tenham a propriedade OptimizedInstallMode definida como 1 (um) na Tabela [MsiPatchMetadata](msipatchmetadata-table.md).

Se um patch modificar apenas as tabelas a seguir, o Windows Installer 3.0 ou posterior ignorará as ações associadas a todas as outras tabelas, mesmo que essas ações sejam listadas nas tabelas de sequência do pacote de instalação do aplicativo original (arquivo .msi).

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condição](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [Arquivo](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Mídia](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [Patch](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [Propriedade](property-table.md)
-   [Registro](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [Typelib](typelib-table.md)
-   [\_Colunas](-columns-table.md)
-   [\_Armazenamentos](-storages-table.md)
-   [\_Fluxos](-streams-table.md)
-   [\_Tabelas](-tables-table.md)
-   [\_Tabela TransformView](-transformview-table.md)
-   [\_Validação](-validation-table.md)

Para desativar a opção de otimização de patch, use a [política DisableFlyWeightPatching.](disableflyweightpatching.md)

 

 



