---
description: O mapeamento de arquivo pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos. Para compartilhar um arquivo ou uma memória, todos os processos devem usar o nome ou o identificador do mesmo objeto de mapeamento de arquivo.
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: Compartilhando arquivos e memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647206"
---
# <a name="sharing-files-and-memory"></a>Compartilhando arquivos e memória

O mapeamento de arquivo pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos. Para compartilhar um arquivo ou uma memória, todos os processos devem usar o nome ou o identificador do mesmo objeto de mapeamento de arquivo.

Para compartilhar um arquivo, o primeiro processo cria ou abre um arquivo usando a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Em seguida, ele cria um objeto de mapeamento de arquivo usando a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) , especificando o identificador de arquivo e um nome para o objeto de mapeamento de arquivo. Os nomes dos objetos evento, semáforo, mutex, temporizador de espera, trabalho e mapeamento de arquivo compartilham o mesmo namespace. Portanto, as funções **CreateFileMapping** e [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) falharão se especificarem um nome que está sendo usado por um objeto de outro tipo.

Para compartilhar memória que não está associada a um arquivo, um processo deve usar a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) e especificar um \_ valor de identificador inválido \_ como o parâmetro *hFile* em vez de um identificador de arquivo existente. O objeto de mapeamento de arquivo correspondente acessa a memória apoiada pelo arquivo de paginação do sistema. Você deve especificar um tamanho maior que zero quando especificar um *hFile* de valor de \_ identificador inválido \_ em uma chamada para **CreateFileMapping**.

A maneira mais fácil de outros processos obter um identificador do objeto de mapeamento de arquivo criado pelo primeiro processo é usar a função [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) e especificar o nome do objeto. Isso é conhecido como *memória compartilhada nomeada*. Se o objeto de mapeamento de arquivo não tiver um nome, o processo deverá obter um identificador para ele por meio de herança ou duplicação. Para obter mais informações sobre a herança e a duplicação, consulte [herança](../procthread/inheritance.md).

Os processos que compartilham arquivos ou memória devem criar exibições de arquivo usando a função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) ou [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) . Eles devem coordenar o acesso usando semáforos, mutexes, eventos ou alguma outra técnica de exclusão mútua. Para obter mais informações, consulte [sincronização](../sync/synchronization.md).

Um objeto de mapeamento de arquivo compartilhado não será destruído até que todos os processos que o usam fechem seus identificadores para ele usando a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

Para obter informações sobre segurança de objeto de mapeamento de arquivo, consulte [segurança de mapeamento de arquivo e direitos de acesso](file-mapping-security-and-access-rights.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando a memória compartilhada nomeada](creating-named-shared-memory.md)
</dt> </dl>

 

 
