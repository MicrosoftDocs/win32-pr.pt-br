---
description: Constantes do VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes do VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787027"
---
# <a name="vds-constants"></a>Constantes do VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

As constantes do VDS são categorizadas da seguinte maneira:

-   [Constantes de status do objeto](#object-status-constants)
-   [Constantes de dicas do automagic](#automagic-hints-constants)
-   [Constantes diversas](#miscellaneous-constants)

### <a name="object-status-constants"></a>Constantes de status do objeto



| Constante           | Valor |
|--------------------|-------|
| STATUS \_ desconhecido    | 0     |
| STATUS \_ online     | 1     |
| o STATUS \_ não \_ está pronto | 2     |
| STATUS \_ sem \_ mídia  | 3     |
| STATUS \_ offline    | 4     |
| \_falha no status     | 5     |
| STATUS \_ ausente    | 6     |



 

### <a name="automagic-hints-constants"></a>Constantes de dicas do automagic



| Constante                               | Valor   |
|----------------------------------------|---------|
| Dica de VDS \_ \_ MOSTLYREADS                 | 0x0002L |
| Dica de VDS \_ \_ OPTIMIZEFORSEQUENTIALREADS  | 0x0004L |
| Dica de VDS \_ \_ OPTIMIZEFORSEQUENTIALWRITES | 0x0008L |
| Dica de VDS \_ \_ REMAPENABLED                | 0x0020L |
| Dica de VDS \_ \_ WRITETHROUGHCACHINGENABLED  | 0x0040L |
| Dica de VDS \_ \_ HARDWARECHECKSUMENABLED     | 0x0080L |
| Dica de VDS \_ \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Constantes diversas



| Constante                     | Valor      |
|------------------------------|------------|
| \_ \_ prioridade mínima da recompilação do VDS \_  | 0x0001L    |
| \_informações de \_ LUN do VDS da versão \_   | 1          |
| comprimento máximo de \_ ComputerName \_    | 15         |
| comprimento máximo de \_ PROVIDERNAME \_    | 200        |
| comprimento máximo de \_ VersionString \_   | 16         |
| letra da unidade \_ \_ prop          | N/D        |
| tamanho máximo do \_ \_ nome FS \_          | 8          |
| \_membro \_ IDX inválido         | 0xFFFFFFFF |
| \_comprimento do \_ nome da partição GPT \_ | 36         |
| \_caminho máximo                    | 260        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do VDS](vds-reference.md)
</dt> </dl>

 

 
