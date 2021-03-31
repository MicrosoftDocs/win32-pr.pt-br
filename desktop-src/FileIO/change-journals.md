---
description: Quando qualquer alteração é feita em um arquivo ou diretório em um volume, o diário de alterações do USN desse volume é atualizado com uma descrição da alteração e o nome do arquivo ou diretório.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Diários de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837007"
---
# <a name="change-journals"></a>Diários de alterações

Um aplicativo de backup automático é um exemplo de um programa que deve verificar se há alterações no estado de um volume para executar sua tarefa. O método de força bruta de verificar alterações em diretórios ou arquivos é verificar todo o volume. No entanto, isso geralmente não é uma abordagem aceitável devido à redução no desempenho do sistema que ela causaria. Outro método é para o aplicativo registrar uma notificação de diretório (chamando as funções [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) ou [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ) para os diretórios cujo backup será feito. Isso é mais eficiente do que o primeiro método, no entanto, requer que um aplicativo seja executado o tempo todo. Além disso, se for necessário fazer backup de um grande número de diretórios e arquivos, a quantidade de processamento e a sobrecarga de memória para tal aplicativo também podem causar a diminuição do desempenho do sistema operacional.

Para evitar essas desvantagens, o sistema de arquivos NTFS mantém um diário de alterações de USN (número de sequência de atualização). Quando qualquer alteração é feita em um arquivo ou diretório em um volume, o diário de alterações do USN desse volume é atualizado com uma descrição da alteração e o nome do arquivo ou diretório.

Os diários de alterações também são necessários para recuperar a indexação do sistema de arquivos, por exemplo, após uma falha de computador ou volume. A capacidade de recuperar a indexação significa que o sistema de arquivos pode evitar o processo demorado de reindexação de todo o volume nesses casos.

Os tópicos a seguir discutem os diários de alterações.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                             | Descrição                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alterar registros do diário](change-journal-records.md)<br/>                                                                   | Como arquivos, diretórios e outros objetos do sistema de arquivos NTFS são adicionados, excluídos e modificados, o sistema de arquivos NTFS insere registros de diário de alterações em fluxos, um para cada volume no computador.<br/>                                           |
| [Usando o identificador do diário de alterações](using-the-change-journal-identifier.md)<br/>                                         | O sistema de arquivos NTFS associa um identificador não assinado de 64 bits a cada diário de alterações.<br/>                                                                                                                                                   |
| [Criando, modificando e excluindo um diário de alterações](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Os administradores podem criar, excluir e recriar diários de alterações.<br/>                                                                                                                                                                         |
| [Obtendo um identificador de volume para operações de diário de alterações](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Para obter um identificador para um volume para uso com operações de diário de alteração de número de sequência de atualização (USN), chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o parâmetro *lpFileName* definido como uma cadeia de caracteres do seguinte formato: \\ \\ . \\ *X*.<br/> |
| [Operações de diário de alterações](change-journal-operations.md)<br/>                                                             | Códigos de controle e estruturas para usar com o diário de alterações do USN (número de sequência de atualização) do sistema de arquivos NTFS.<br/>                                                                                                                                |



 

 

 




