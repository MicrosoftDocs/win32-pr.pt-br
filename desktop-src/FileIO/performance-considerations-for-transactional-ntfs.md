---
description: Recomendações para transações de sistema de arquivos ideais.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Considerações de desempenho para NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32729725ecc6ba59808eabe1fa12a5b798c9413c52d1591bd22b498e6a5856d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996710"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Considerações de desempenho para NTFS Transacional

O NTFS Transacional (TxF) foi cuidadosamente projetado para desempenho e normalmente funcionará melhor do que as alternativas transacionais de uso geral em cenários semelhantes. No entanto, as transações do sistema de arquivos têm mais sobrecarga do que as operações não transacionadas, e alguma redução no desempenho de e/s em comparação com e/s não transacionada é esperada. Os aplicativos de desempenho crítico devem executar um ciclo de qualificação de adoção de tecnologia, avaliando o impacto no desempenho das operações do sistema de arquivos transacionais.

## <a name="overview-of-txf-operations"></a>Visão geral das operações de TxF

O TxF usa o registro em log de *desfazer* para registrar as alterações necessárias para colocar o sistema de arquivos novamente em um estado consistente, também conhecido como reversão, caso uma anulação de transação ocorra. Esse log de desfazer gera e/s adicional e é a origem da sobrecarga de desempenho de TxF em comparação com operações de sistema de arquivos não transacionais.

Um resumo de alto nível de como o TxF Opera é o seguinte:

-   À medida que uma transação progride, o TxF grava registros de *desfazer* em seu arquivo de log para cada modificação que faz no sistema de arquivos. Se ocorrer uma anulação, esses registros de desfazer serão analisados para colocar o sistema de arquivos novamente no estado em que estava antes do início da transação.
-   Um registro de desfazer de *alteração de metadados* descreve uma alteração somente nos metadados do sistema de arquivos. Alguns exemplos disso são movimentações, renomeações, acréscimos e alterações de atributo. Para registros de desfazer alteração de metadados, todas as informações necessárias para desfazer a alteração estão no registro e armazenadas no arquivo de log.
-   Um registro de desfazer *substituição* descreve uma substituição de uma parte de um arquivo. Quando ocorre uma substituição de arquivo, o conteúdo original do arquivo é armazenado em um arquivo de desfazer especial em um diretório oculto e os pontos de registro de desfazer de substituição para esse arquivo. Quando as atualizações de arquivo são eventualmente liberadas do cache para o disco, o conteúdo do arquivo de desfazer também deve ser liberado e, portanto, uma substituição de arquivo transacionado poderia gerar até duas operações de e/s aleatórias extras: uma para ler os dados antigos e um para gravá-lo no arquivo de desfazer. Essas operações de e/s extras são um custo de desempenho de TxF.
-   Quando ocorre uma confirmação, o TxF primeiro libera Todas as informações de desfazer e, em seguida, libera as alterações reais do arquivo e, em seguida, grava e libera um registro de confirmação. Se não houver nenhum arquivo de desfazer a ser liberado, a única sobrecarga adicional de TxF relativa à e/s não transacionada será a própria liberação de log. No entanto, as liberações de log resultam em grandes gravações sequenciais eficientes para que o custo de desempenho seja mínimo.
-   O TxF é otimizado para confirmação. Espera-se que a maioria das transações seja bem sucedido e não precise ser revertida, portanto, espera-se que todos os registros de desfazer de uma transação fiquem inutilizados. Do ponto de vista do desempenho, as operações de confirmação do TxF são rápidas e as reversões são de uso intensivo de recursos.
-   A reversão é mais intensiva em recursos do que a confirmação. Durante a reversão, todas as alterações feitas na transação precisam ser desfeitas. Em geral, a duração da reversão pode ser aproximadamente a mesma tomada para fazer as alterações originalmente. Por exemplo, se levou 1 segundo para fazer todas as alterações, poderia levar cerca de 1 segundo para desfazê-las. Para transações muito longas, a reversão pode criar impactos de desempenho adicionais. Por exemplo, o tempo de inicialização do sistema pode ser atrasado se o sistema precisar reverter automaticamente uma transação caso o sistema pare de responder e deva executar uma reinicialização não agendada.

As conclusões de resumo sobre o desempenho que podem ser desenhadas da lista anterior são as seguintes:

-   O custo de desempenho do TxF para transações que envolvem substituições de arquivo pode ser significativo.
-   O custo de desempenho do TxF para transações que envolvem apenas operações de metadados pode ser relativamente baixo, desde que sejam usadas transações grandes. Uma transação grande é quando há muitos registros de desfazer para cada registro de confirmação.

## <a name="recommendations-for-best-performance"></a>Recomendações Para obter o melhor desempenho

Amortizar a sobrecarga de TxF em transações maiores. Por exemplo, se você tiver *N* conjuntos de alterações para fazer onde cada alteração tem *M* etapas e tiver a opção de fazer isso como *N* transações de *m* etapas cada ou fazer tudo como uma única transação com *M* \* *N* etapas, a última opção seria mais eficiente.

Considere o possível impacto na inicialização de transações muito grandes. Conforme indicado anteriormente, a reversão pode ser lenta e atrasará o tempo de inicialização se o sistema precisar executar reversões automáticas como tempo de inicialização. Quanto maior a transação, mais tempo o atraso.

Manter as transações para a maioria das operações de metadados. É para isso que o TxF é otimizado para e, em geral, o desempenho é quase igual à e/s de arquivo não transacionado para transações de metadados grandes. Exemplos de funções do TxF de metadados eficientes são [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda), [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda), [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda), [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda), [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)e gravações acrescentadas (chamadas para a função [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) quando o ponteiro do arquivo for no final do arquivo ou *EOF*). Um exemplo de operações de não metadados com uso intensivo de recursos são chamadas para a função **WriteFile** quando o ponteiro do arquivo não está no EOF.

## <a name="summary-of-txf-performance-expectations"></a>Resumo das expectativas de desempenho de TxF

Para atualizações in-loco, as substituições em uma seção de um arquivo serão muito mais lentas do que a e/s de arquivo não transacionado, enquanto o desempenho do TxF para operações de metadados do sistema de arquivos (por exemplo, criar, mover e acrescentar) é comparável a e/s de arquivo não transacionado para transações grandes.

 

 



