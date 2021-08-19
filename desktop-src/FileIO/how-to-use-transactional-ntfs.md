---
description: Gerenciamento de alças de arquivo transacionado em NTFS transacional.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Como usar NTFS transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8daafd2bc2ee0e695ee3bdede4ac2f62be1000c111d0c544dec877c357f42629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015274"
---
# <a name="how-to-use-transactional-ntfs"></a>Como usar NTFS transacional

## <a name="transacted-file-handles"></a>Alças de arquivo transacionado

O NTFS transacional (TxF) vincula um alça de arquivo a uma transação. Para operações que funcionam em um handle (por exemplo, as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile),**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) a chamada de função de API real não é muda. Para operações de arquivo que têm um nome, há funções transacionados explícitas para essas operações. Por exemplo, em vez de chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), chame [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Isso cria um alça de arquivo transacionado, que pode ser usado para todas as operações de arquivo que exigem um handle. Todas as operações subsequentes que usam esse handle são operações transacionados.

## <a name="basic-txf-usage"></a>Uso básico do TxF

A série de etapas a seguir representa o uso mais básico do TxF. Também há suporte para cenários mais complexos, a critério do designer de aplicativos.

1.  Crie uma transação chamando a função KTM [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) ou usando a interface **IKernelTransaction** do [Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Obter os handle(s) de arquivo transacionado chamando [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Modifique os arquivos conforme necessário usando os alças de arquivo transacionados.
4.  Feche todos os alças de arquivo transacionado associados à transação criada na etapa 1.
5.  Confirma ou anula a transação chamando a função KTM ou DTC correspondente.

## <a name="key-points-of-the-txf-programming-model"></a>Principais pontos do modelo de programação TxF

O modelo de programação TxF tem os seguintes pontos principais a considerar ao desenvolver um aplicativo TxF:

-   É altamente recomendável que um aplicativo feche todos os tratamentos de arquivo transacionado antes de comprometer ou reverter uma transação. O sistema invalida todos os alças transacionados quando uma transação termina. Qualquer operação, exceto fechar, executada em um handle transacionado após o encerramento da transação retorna o seguinte erro: **ERROR HANDLE NÃO É MAIS \_ \_ \_ \_ VÁLIDO.**
-   Um arquivo é exibido como uma unidade de armazenamento. Há suporte para atualizações parciais e substituições completas de arquivo. Várias transações não podem modificar simultaneamente o mesmo arquivo.
-   A E/S mapeada na memória é transparente e consistente com a E/S de arquivo normal. Um aplicativo deve liberar e fechar uma seção aberta antes de comprometer uma transação. A falha ao fazer isso pode resultar em alterações parciais no arquivo mapeado dentro da transação. Uma reação falhará se isso não for feito.

## <a name="common-programming-errors"></a>Erros comuns de programação

Os seguintes erros comuns podem ocorrer ao desenvolver aplicativos transacionados:

-   Usando um alça de arquivo após a conclusão de uma transação.
-   Falha ao fechar os alças para arquivos e diretórios excluídos antes de comprometer uma transação, o que impedirá que as operações de exclusão ocorram. Esse evento deve ocorrer antes de executar a confirmação para que a operação de exclusão seja considerada parte da transação. Isso ocorre porque, na verdade, o sistema não exclui um arquivo até que o último lidar com ele seja fechado, mesmo quando a operação não é transatada, como parte do subsistema de E/S do arquivo Windows.
-   Falha ao levar em conta as reações de transação iniciadas pelo sistema, o que pode ocorrer a qualquer momento; por exemplo, uma transação será re roll back se os recursos do sistema se esgotarem.

 

 
