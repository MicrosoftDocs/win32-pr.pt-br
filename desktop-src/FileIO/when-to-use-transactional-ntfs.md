---
description: Use o NTFS transacional para manter a integridade dos dados.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Quando usar o NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783308"
---
# <a name="when-to-use-transactional-ntfs"></a>Quando usar o NTFS Transacional

Um aplicativo pode usar o NTFS Transacional (TxF) para preservar a integridade dos dados em disco durante condições de erro inesperadas. Em geral, um aplicativo deve considerar o uso do TxF se o aplicativo estiver liberando arquivos e usando outras técnicas para manter a integridade dos dados. O TxF pode executar melhor e simplificar o código de tratamento de erros do aplicativo, aumentando a recuperação e a confiabilidade do erro. As seções a seguir neste tópico fornecem exemplos de cenários para usar o TxF.

## <a name="updating-a-file"></a>Atualizando um arquivo

A atualização de um arquivo é uma operação comum e normalmente simples. No entanto, se o sistema ou aplicativo falhar enquanto um aplicativo estiver atualizando informações em um disco, o resultado poderá ser catastrófico, pois os dados do usuário podem ser corrompidos por uma operação de atualização de arquivo parcialmente concluída. Aplicativos robustos geralmente executam sequências complexas de cópias de arquivos e renomeações de arquivo para garantir que os dados não sejam corrompidos se um sistema falhar.

O TxF torna simples para um aplicativo proteger as operações de atualização de arquivos contra falhas do sistema ou do aplicativo. Para atualizar um arquivo com segurança, o aplicativo abre o arquivo no modo transacionado, faz as atualizações necessárias e, em seguida, confirma a transação. Se o sistema ou aplicativo falhar durante a atualização do arquivo, o TxF restaura automaticamente o arquivo para o estado que ele tinha antes do início da atualização do arquivo, o que evita a corrupção do arquivo.

## <a name="multi-file-updates"></a>Atualizações de vários arquivos

O TxF é ainda mais importante quando uma única operação lógica afeta vários arquivos. Por exemplo, se você quiser usar uma ferramenta para renomear uma das páginas HTML ou ASP em um site, uma ferramenta bem projetada também corrigirá todos os links para usar o novo nome de arquivo. No entanto, uma falha durante essa operação deixa o site em um estado inconsistente, com alguns dos links que ainda se referem ao nome do arquivo antigo. Ao fazer a operação de renomeação de arquivo e o link que está corrigindo a operação de uma única transação, o TxF garante que a correção do arquivo e o link sejam bem-sucedidos ou falhem como uma única operação.

## <a name="consistent-concurrent-updates"></a>Atualizações simultâneas consistentes

O TxF isola as transações simultâneas. Se um aplicativo abrir um arquivo para uma leitura transacional enquanto outro aplicativo tiver o mesmo arquivo aberto para uma atualização transacional, o TxF isolará os efeitos das duas transações entre si. Em outras palavras, o leitor transacional sempre exibe uma única versão consistente do arquivo, mesmo que esse arquivo esteja em processo de ser atualizado por outra transação.

Um aplicativo pode usar essa funcionalidade para permitir que os clientes exibam arquivos enquanto outros clientes fazem atualizações. Por exemplo, um servidor Web transacional pode fornecer uma exibição única e consistente de arquivos enquanto outra ferramenta atualiza esses arquivos simultaneamente.

> [!Note]  
> O TxF não oferece suporte a atualizações simultâneas por vários gravadores em transações diferentes. O TxF dá suporte a apenas um único gravador com vários leitores simultâneos e consistentes.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordenando com outros gerenciadores de recursos transacionados

As transações usadas com sistemas de arquivos transacionados também podem ser usadas com o registro transacionado. As atualizações no arquivo e no registro são coordenadas com uma única transação.

Ao usar transações de [Coordenador de transações distribuídas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) ou System. Transactions, as atualizações feitas no SQL, no MSMQ e em outros recursos transacionais podem ser coordenadas com atualizações de arquivo realizadas. Para obter mais informações, consulte [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))do DTC.

## <a name="unsupported-scenarios"></a>Cenários sem suporte

O TxF não dá suporte aos seguintes cenários de transação:

-   Transações em volumes de rede, por exemplo, em compartilhamentos de arquivos. Não há suporte para TxF nos protocolos CIFS/SMB.
-   Transações em qualquer sistema de arquivos que não sejam NTFS.
-   Operações transacionadas em arquivos armazenados em cache pelo armazenamento em cache do lado do cliente.
-   Acesso ao arquivo usando IDs de objeto.
-   Qualquer cenário de gravador compartilhado.
-   Qualquer situação em que um arquivo é aberto por um período de tempo estendido (dias ou semanas).

 

 
