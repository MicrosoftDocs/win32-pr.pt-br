---
description: Terminologia usada para descrever o NTFS Transacional (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossário do TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171500"
---
# <a name="txf-glossary"></a>Glossário do TxF

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**ininterrupta**
</dt> <dd>

Disponibilidade significa que um Gerenciador de recursos anulará as transações mesmo que isso interrompa a consistência para que o sistema possa continuar a fazer um novo trabalho. O Gerenciador de recursos padrão força a disponibilidade no volume do sistema. Por exemplo, se o log de transações estiver cheio, o novo espaço de log de transações não poderá ser adicionado e uma transação mais antiga que seria anulada exigirá que um resultado seja entregue de um Gerenciador de recursos superior para que uma transação distribuída seja concluída, o Gerenciador de recursos não aguardará o Gerenciador de transações superior e anulará essa transação, mesmo que possa interromper a consistência.

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**verificação**
</dt> <dd>

Consistência significa que um Gerenciador de recursos falhará em novas transações se não puder fazer o progresso. Por exemplo, se o log de transações estiver cheio, o novo espaço de log de transações não poderá ser adicionado e uma transação mais antiga que seria anulada exigirá a entrega de um resultado de um Gerenciador de recursos superior para que uma transação distribuída seja concluída, o Gerenciador de recursos aguardará esse resultado.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversão**
</dt> <dd>

Um miniversão é uma versão de um arquivo que um gravador transacionado cria durante uma transação. O miniversão pode ser aberto posteriormente na transação com acesso somente leitura.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**leitor transacionado**
</dt> <dd>

Um leitor transacionado é um identificador de arquivo transacionado aberto com qualquer permissão que faça parte do acesso de leitura genérico, mas que não faz parte do acesso de gravação genérico.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**gravador transacionado**
</dt> <dd>

Um gravador transacionado é um identificador de arquivo transacionado aberto com qualquer permissão que não faça parte do acesso de leitura genérico, mas que faz parte do acesso de gravação genérico.

</dd> </dl>

 

 



