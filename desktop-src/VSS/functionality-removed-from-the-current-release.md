---
description: 'a versão 2003 do VSS do Windows Server não dá mais suporte ao seguinte:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: funcionalidade removida do Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7cd2cbfce24717bdd0bf0c36db1c5d8ff7faddebd5b7795cff6640b74df3c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006356"
---
# <a name="functionality-removed-from-windows-server-2003"></a>funcionalidade removida do Windows Server 2003

a versão 2003 do VSS do Windows Server não dá mais suporte ao seguinte:

-   Os gravadores não podem especificar novos destinos de restauração de arquivo ([*novos locais de destino*](vssgloss-n.md)) em operações de restauração.
-   Não há mais suporte para a remontagem de uma cópia de sombra exposta como um volume gravável. O método **IVssBackupComponents:: RemountReadWrite** não está mais disponível.
-   Os gravadores não podem especificar arquivos explicitamente incluídos (usando [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Os arquivos podem ser adicionados a um componente somente como parte de um conjunto de arquivos usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    Os arquivos ainda podem ser explicitamente excluídos de um componente usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



