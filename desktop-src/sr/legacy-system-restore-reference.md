---
title: Referência de restauração do sistema herdada
description: Esta documentação descreve os detalhes de implementação do repositório usado por uma versão herdada da restauração do sistema. Ele não se aplica à implementação da restauração do sistema no Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822289"
---
# <a name="legacy-system-restore-reference"></a>Referência de restauração do sistema herdada

\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]

Esta documentação descreve os detalhes de implementação do repositório usado por uma versão herdada da restauração do sistema. Ele não se aplica à implementação da restauração do sistema no Windows Vista.

## <a name="system-restore-repository-structure"></a>Estrutura do repositório de restauração do sistema

O Windows XP com SP2 contém um repositório para a restauração do sistema na seguinte pasta:% SYSTEMDRIVE% \\ informações de volume do sistema. Esse repositório contém informações para pontos de restauração, que são essencialmente um instantâneo do sistema em um momento no tempo.

O repositório é estruturado da seguinte maneira:

Restauração de **informações de volume do sistema**    ** \_ {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n** *     ** \_ Restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n***

Para determinar qual \_ pasta de restauração {*GUID*} usar, leia o **GUID** especificado no seguinte arquivo: SYSTEMROOT% \\ System32 \\ Restore \\MachineGUID.txt.

Dentro de cada \_ pasta Restore {*GUID*}, o \_ arquivo Driver. cfg contém informações de uma estrutura de **configuração do Sr \_ persistent \_** definida da seguinte maneira:

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>Arquivos contidos em cada pasta RP *n*

Cada pasta RP *n* contém uma pasta de instantâneo que contém o seguinte:

-   Um instantâneo dos hives do registro
-   Uma pasta de repositório que contém um instantâneo do repositório WMI
-   Um instantâneo do banco de dados COM+
-   Um instantâneo do banco de dados do IIS

Cada pasta RP *n* contém um arquivo RP. log que contém informações gerais sobre o ponto de restauração da estrutura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .

Cada pasta RP *n* pode conter arquivos usados para controlar as alterações de um ponto de restauração. O primeiro arquivo é chamado Change. log, o próximo arquivo é chamado Change. log. 1 e assim por diante. Cada arquivo de log de alterações contém as seguintes estruturas:

-   [**ALTERAR \_ cabeçalho do log \_**](change-log-header.md)
-   [**Alterar \_ \_Entrada de log**](change-log-entry.md)1
-   [**Alterar \_ \_Entrada de log**](change-log-entry.md)2
-   ...
-   [**Alterar \_ \_Entrada de log**](change-log-entry.md)*n*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas de restauração do sistema herdadas](legacy-system-restore-structures.md)
</dt> </dl>

 

 




