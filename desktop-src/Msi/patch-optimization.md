---
description: Windows Installer pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches aos aplicativos instalados.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Otimização de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827869"
---
# <a name="patch-optimization"></a>Otimização de patch

Windows Installer pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches aos aplicativos instalados.

**Windows Installer 2,0:** Sem suporte. Para versões do Windows Installer lançadas antes de Windows Installer 3,0, a aplicação de patches executa uma instalação de reparo completa do aplicativo, o que pode levar muito mais tempo.

**Windows Installer 3,0 e posterior:** O processo de aplicação de patches altera apenas as partes de um aplicativo que são modificadas por um patch.

**Windows Installer 3,1 e posterior:** A partir do Windows Installer 3,1, a otimização de patch requer que todos os patches na transação tenham a propriedade OptimizedInstallMode definida como 1 (um) na [tabela MsiPatchMetadata](msipatchmetadata-table.md).

Se um patch modificar apenas as tabelas a seguir, Windows Installer 3,0 ou posterior ignorará as ações associadas a todas as outras tabelas, mesmo se essas ações estiverem listadas nas tabelas de sequência do pacote de instalação do aplicativo original (arquivo. msi).

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
-   [Importação](typelib-table.md)
-   [\_Columns](-columns-table.md)
-   [\_Armazenamentos](-storages-table.md)
-   [\_Fluxos](-streams-table.md)
-   [\_Tabelas](-tables-table.md)
-   [\_Tabela de transformview](-transformview-table.md)
-   [\_Validação](-validation-table.md)

Para desativar a opção de otimização de patch, use a política [DisableFlyWeightPatching](disableflyweightpatching.md) .

 

 



