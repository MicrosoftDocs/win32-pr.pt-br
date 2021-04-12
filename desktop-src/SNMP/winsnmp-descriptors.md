---
title: Descritores de WinSNMP
description: No ambiente de programação WinSNMP, um descritor é uma das duas estruturas a seguir.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291890"
---
# <a name="winsnmp-descriptors"></a>Descritores de WinSNMP

No ambiente de programação WinSNMP, um *descritor* é uma das duas estruturas a seguir:

-   Uma estrutura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) que descreve uma variável de cadeia de caracteres de octeto
-   Uma estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) que descreve uma variável de identificador de objeto SNMP

Um descritor de WinSNMP é uma estrutura que tem dois membros: um membro de comprimento, **Len** e um membro de ponteiro, **PTR**. O membro **PTR** aponta para a cadeia de caracteres de octeto ou o identificador de objeto de interesse. O membro **PTR** pode ser o tipo de dados **smiLPBYTE** ou **smiLPUINT32** .

Um descritor de [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou um descritor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) pode ser o membro de **valor** de uma estrutura **smiVALUE** . A estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) descreve o valor associado a um nome de variável em uma entrada de associação de variável.

A implementação do Microsoft WinSNMP aloca e desaloca memória para todas as estruturas **smiOCTETS** e **smiOID** de saída. Portanto, o aplicativo deve chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar a memória para o membro **PTR** dessas estruturas.

Membros de cadeia de caracteres nos descritores não exigem um byte de terminação **nulo** . Para obter informações adicionais sobre como gerenciar a memória alocada para descritores, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




