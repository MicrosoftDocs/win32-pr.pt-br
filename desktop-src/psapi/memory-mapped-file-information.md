---
title: Informações do arquivo de Memory-Mapped
description: Um arquivo mapeado para memória (ou mapeamento de arquivo) é o resultado da Associação de um conteúdo de arquivo com uma parte do espaço de endereço virtual de um processo. Ele pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084804"
---
# <a name="memory-mapped-file-information"></a>Informações do arquivo de Memory-Mapped

Um *arquivo mapeado para memória* (ou *mapeamento de arquivo*) é o resultado da Associação de um conteúdo de arquivo com uma parte do espaço de endereço virtual de um processo. Ele pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos.

A função [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) recebe um identificador de processo e um ponteiro para um endereço como entrada. Se o endereço estiver dentro de um arquivo mapeado por memória no espaço de endereço virtual do processo, a função retornará o nome do arquivo mapeado para a memória. Os nomes de arquivo retornados por **GetMappedFileName** usam o formulário de dispositivo, em vez de letras de unidade. Por exemplo, o nome do arquivo c: \\ WinNT \\ System32 \\ CType. NLS teria esta aparência no formato do dispositivo:

\\Device \\ Harddisk0 \\ Partition1 \\ WinNT \\ System32 \\ CType. NLS

Para obter mais informações sobre arquivos mapeados para memória, consulte [mapeamento de arquivo](/windows/desktop/Memory/file-mapping). Para obter um exemplo que converte nomes de arquivo em formato de dispositivo em letras de unidade, consulte [obtendo um nome de arquivo de um identificador de arquivo](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).

 

 