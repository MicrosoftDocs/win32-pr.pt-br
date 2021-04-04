---
description: O espaço de endereço virtual do sistema (VA) em sistemas de 32 bits pode se esgotar devido à fragmentação. Várias chaves do registro podem ser usadas para configurar limites de memória em sistemas de 32 bits que apresentam esse problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Chaves do registro de gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837412"
---
# <a name="memory-management-registry-keys"></a>Chaves do registro de gerenciamento de memória

O espaço de endereço virtual do sistema (VA) em sistemas de 32 bits pode se esgotar devido à fragmentação. Várias chaves do registro podem ser usadas para configurar limites de memória em sistemas de 32 bits que apresentam esse problema. O espaço do sistema VA nos sistemas de 64 bits não está sujeito ao esgotamento por fragmentação; Portanto, essas chaves não têm nenhum efeito nos sistemas de 64 bits.

Para sistemas de 32 bits, essas chaves do registro de gerenciamento de memória devem ser explicitamente criadas na seguinte chave do registro:

**HKEY \_ \_** Gerenciamento de controle de \\  \\  \\  \\  \\ **memória** do Gerenciador de sessão de controle atual do sistema de máquina local

**Windows Server 2008 e Windows Vista:** Essas chaves do registro estão disponíveis em sistemas de 32 bits que começam com o Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1).

Para limites de espaço de endereço e memória padrão em sistemas de 32 bits e 64 bits, consulte [limites de memória para versões do Windows](memory-limits-for-windows-releases.md).

A tabela a seguir descreve as chaves do registro de gerenciamento de memória que podem ser usadas para configurar limites de memória em sistemas de 32 bits. Todas essas chaves têm um tipo REG \_ DWORD e valores possíveis que variam de 0 a 2.048 MB. O padrão é 0, o que significa que nenhum limite é imposto. Os valores são arredondados automaticamente para o próximo limite de alocação do sistema VA, que é de 2 MB em sistemas de 32 bits que têm a [extensão de endereço físico](physical-address-extension.md) (PAE) habilitada e 4 MB em sistemas de 32 bits que não têm a PAE habilitada.



| Chave                   | Descrição                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo pool não paginável. Em determinadas condições, esse limite pode ser excedido por uma pequena quantidade. |
| **PagedPoolLimit**    | Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo pool paginável.                                                                            |
| **SessionSpaceLimit** | Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada por alocações de espaço de sessão.                                                                 |
| **SystemCacheLimit**  | Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo cache do sistema. Em determinadas condições, esse limite pode ser excedido por uma pequena quantidade.  |
| **SystemPtesLimit**   | Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada por mapeamentos de e/s e outros recursos que consomem PTEs (entradas de tabela de página do sistema).            |



 

Determinar se o espaço do sistema VA está sendo esgotado requer o uso de um depurador de kernel. Para obter mais informações, consulte [Ferramentas de depuração para Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



