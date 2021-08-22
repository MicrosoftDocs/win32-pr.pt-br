---
description: Use NTFS transacional para manter a integridade dos dados.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Quando usar NTFS transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f7a67fe6960a8754f768956457afbd04a509bbf9a3c18360b4651e4d9ccda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830126"
---
# <a name="when-to-use-transactional-ntfs"></a>Quando usar NTFS transacional

Um aplicativo pode usar O TxF (Transactional NTFS) para preservar a integridade dos dados no disco durante condições de erro inesperadas. Em geral, um aplicativo deve considerar o uso do TxF se o aplicativo estiver liberando arquivos e usando outras técnicas para manter a integridade dos dados. O TxF pode ter um desempenho melhor e simplificar o código de tratamento de erros do aplicativo, melhorando a recuperação de erros e a confiabilidade. As seções a seguir neste tópico fornecem exemplos de cenários para você usar o TxF.

## <a name="updating-a-file"></a>Atualizando um arquivo

A atualização de um arquivo é uma operação comum e normalmente simples. No entanto, se o sistema ou aplicativo falhar enquanto um aplicativo estiver atualizando informações em um disco, o resultado poderá ser catastrófico, pois os dados do usuário podem ser corrompidos por uma operação de atualização de arquivo parcialmente concluída. Aplicativos robustos geralmente executam sequências complexas de cópias de arquivo e renomeações de arquivo para garantir que os dados não serão corrompidos se um sistema falhar.

O TxF torna simples para um aplicativo proteger operações de atualização de arquivo contra falhas do sistema ou do aplicativo. Para atualizar um arquivo com segurança, o aplicativo abre o arquivo no modo transacionado, faz as atualizações necessárias e confirma a transação. Se o sistema ou o aplicativo falhar durante a atualização do arquivo, o TxF restaurará automaticamente o arquivo para o estado que tinha antes do início da atualização do arquivo, o que evita a corrupção do arquivo.

## <a name="multi-file-updates"></a>Atualizações de vários arquivos

O TxF é ainda mais importante quando uma única operação lógica afeta vários arquivos. Por exemplo, se você quiser usar uma ferramenta para renomear uma das páginas HTML ou ASP em um site, uma ferramenta bem projetada também corrigirá todos os links para usar o novo nome de arquivo. No entanto, uma falha durante essa operação deixa o site em um estado inconsistente, com alguns dos links ainda se referindo ao nome de arquivo antigo. Ao tornar a operação de renomear o arquivo e a operação de correção de link uma única transação, o TxF garante que o arquivo renomeado e a correção de link são bem-sucedidos ou falham como uma única operação.

## <a name="consistent-concurrent-updates"></a>Atualizações simultâneas consistentes

O TxF isola transações simultâneas. Se um aplicativo abrir um arquivo para uma leitura transacional enquanto outro aplicativo tiver o mesmo arquivo aberto para uma atualização transacional, o TxF isolará os efeitos das duas transações entre si. Em outras palavras, o leitor transacional sempre visualiza uma única versão consistente do arquivo, mesmo enquanto esse arquivo está em processo de atualização por outra transação.

Um aplicativo pode usar essa funcionalidade para permitir que os clientes possam exibir arquivos enquanto outros clientes fazem atualizações. Por exemplo, um servidor Web transacional pode fornecer uma exibição única e consistente de arquivos, enquanto outra ferramenta atualiza simultaneamente esses arquivos.

> [!Note]  
> O TxF não dá suporte a atualizações simultâneas por vários autores em transações diferentes. O TxF dá suporte a apenas um único autor com vários leitores simultâneos e consistentes.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordenando com outros gerenciadores de recursos transacionados

As transações usadas com sistemas de arquivos transacionados também podem ser usadas com o registro transacionado. As atualizações no arquivo e no Registro são coordenadas com uma única transação.

Usando transações [Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) ou System.Transactions, as atualizações feitas no SQL, no MSMQ e em outros recursos transacionais podem ser coordenadas com atualizações de arquivo transacionados. Para obter mais informações, consulte [IKernelTransaction do DTC.](/previous-versions/windows/desktop/aa344210(v=vs.85))

## <a name="unsupported-scenarios"></a>Cenários sem suporte

O TxF não dá suporte aos seguintes cenários de transação:

-   Transações em volumes de rede, por exemplo, em compartilhamentos de arquivos. O TxF não é suportado pelos protocolos CIFS/SMB.
-   Transações em qualquer sistema de arquivos diferente de NTFS.
-   Operações transacionados em arquivos armazenados em cache pelo cache do lado do cliente.
-   Acesso a arquivos usando IDs de objeto.
-   Qualquer cenário de autor compartilhado.
-   Qualquer situação em que um arquivo é aberto por um longo período de tempo (dias ou semanas).

 

 
