---
description: Gerenciando identificadores de arquivo transacionais em NTFS Transacional.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Como usar o NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778604"
---
# <a name="how-to-use-transactional-ntfs"></a>Como usar o NTFS Transacional

## <a name="transacted-file-handles"></a>Identificadores de arquivo transacionado

O NTFS Transacional (TxF) associa um identificador de arquivo a uma transação. Para operações que funcionam em um identificador (por exemplo, as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ), a chamada de função de API real não é alterada. Para operações de arquivo que recebem um nome, há funções transacionadas explícitas para essas operações. Por exemplo, em vez de chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), chame [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Isso cria um identificador de arquivo transacionado, que pode ser usado para todas as operações de arquivo que exigem um identificador. Todas as operações subsequentes que usam esse identificador são operações transacionadas.

## <a name="basic-txf-usage"></a>Uso básico do TxF

A série de etapas a seguir representa o uso mais básico do TxF. Cenários mais complexos também têm suporte, a critério do designer de aplicativos.

1.  Crie uma transação chamando a função de KTM [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) ou usando a interface **IKernelTransaction** do [Coordenador de transações distribuídas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Obtenha identificadores de arquivo transacionados chamando [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Modifique os arquivos conforme necessário usando o (s) identificador (es) de arquivo transacionado.
4.  Feche todos os identificadores de arquivo transacionados associados à transação criada na etapa 1.
5.  Confirme ou anule a transação chamando a função de KTM ou do DTC correspondente.

## <a name="key-points-of-the-txf-programming-model"></a>Pontos principais do modelo de programação TxF

O modelo de programação TxF tem os seguintes pontos principais a serem considerados ao desenvolver um aplicativo TxF:

-   É altamente recomendável que um aplicativo feche todos os identificadores de arquivo transacionado antes de confirmar ou reverter uma transação. O sistema invalida todos os identificadores transacionados quando uma transação termina. Qualquer operação, exceto fechar, executada em um identificador transacionado após o término da transação retorna o seguinte erro: o **identificador de erro \_ não é \_ \_ mais \_ válido**.
-   Um arquivo é exibido como uma unidade de armazenamento. Há suporte para atualizações parciais e substituições de arquivo completas. Várias transações não podem modificar o mesmo arquivo simultaneamente.
-   A e/s mapeada da memória é transparente e consistente com a e/s de arquivo regular. Um aplicativo deve liberar e fechar uma seção aberta antes de confirmar uma transação. A falha em fazer isso pode resultar em alterações parciais no arquivo mapeado dentro da transação. Uma reversão falhará se isso não for feito.

## <a name="common-programming-errors"></a>Erros comuns de programação

Os seguintes erros comuns podem ocorrer ao desenvolver aplicativos transacionados:

-   Usando um identificador de arquivo após a conclusão de uma transação.
-   Falha ao fechar identificadores para arquivos e diretórios excluídos antes de confirmar uma transação, o que impedirá que as operações de exclusão ocorram. Esse evento deve ocorrer antes de executar a confirmação para que a operação de exclusão seja considerada parte da transação. Isso ocorre porque o sistema não exclui realmente um arquivo até que o último identificador para ele seja fechado, mesmo quando a operação não é transacionada, como parte do subsistema de e/s de arquivo do Windows.
-   Falha ao considerar as reversões de transação iniciadas pelo sistema, o que pode acontecer a qualquer momento; por exemplo, uma transação será revertida se os recursos do sistema estiverem esgotados.

 

 
