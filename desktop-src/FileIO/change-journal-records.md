---
description: Como arquivos, diretórios e outros objetos do sistema de arquivos NTFS são adicionados, excluídos e modificados, o sistema de arquivos NTFS insere registros de diário de alterações em fluxos, um para cada volume no computador.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Alterar registros do diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785468"
---
# <a name="change-journal-records"></a>Alterar registros do diário

Como arquivos, diretórios e outros objetos do sistema de arquivos NTFS são adicionados, excluídos e modificados, o sistema de arquivos NTFS insere registros de diário de alterações em fluxos, um para cada volume no computador. Cada registro indica o tipo de alteração e o objeto alterado. O deslocamento do início do fluxo para um registro específico é chamado de USN (número de sequência de atualização) para o registro específico. Novos registros são acrescentados ao final do fluxo.

O sistema de arquivos NTFS pode excluir registros antigos para conservar espaço. Se os registros necessários tiverem sido excluídos, o serviço de indexação será recuperado ao reindexar o volume, como faz quando não existe um diário de alterações.

O diário de alterações registra apenas o fato de uma alteração em um arquivo e o motivo da alteração (por exemplo, operações de gravação, truncamento, ampliação, exclusão e assim por diante). Ele não registra informações suficientes para permitir a reversão da alteração.

Além disso, várias alterações no mesmo arquivo podem resultar em apenas um sinalizador de motivo sendo adicionado ao registro atual. Se o mesmo tipo de alteração ocorrer mais de uma vez, o sistema de arquivos NTFS não gravará um novo registro para as alterações após o primeiro. Por exemplo, várias operações de gravação sem operações de fechamento e reabertura intermediárias resultam em apenas um registro de alteração com o motivo do sinalizador USN de \_ substituição de dados de motivo \_ \_ .

Para ilustrar como o diário de alterações funciona, suponha que um usuário acesse um arquivo na seguinte ordem:

1.  Grava no arquivo.
2.  Define o carimbo de data/hora do arquivo.
3.  Grava no arquivo.
4.  Trunca o arquivo.
5.  Grava no arquivo.
6.  Fecha o arquivo.

Nesse caso, o sistema de arquivos NTFS executa as seguintes ações no diário de alterações (em que \| indica uma operação ou bit de bits).



| Evento                                 | Ação do sistema de arquivos NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operação de gravação inicial<br/>    | O sistema de arquivos NTFS grava um novo registro USN com o \_ sinalizador USN motivo da \_ substituição de sinalizadores do \_ motivo. Para obter mais informações sobre possíveis sinalizadores de motivo, consulte a estrutura do [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) .<br/>                                                     |
| Configuração do carimbo de data/hora do arquivo<br/> | O sistema de arquivos NTFS grava um novo registro de USN com a configuração de sinalizador definição de dados razão do USN motivo do \_ \_ \_ \| USN \_ motivo da alteração das \_ \_ informações básicas \_ .<br/>                                                                                                                            |
| Segunda operação de gravação<br/>     | O sistema de arquivos NTFS não grava um novo registro USN. Como \_ \_ a substituição de dados do motivo do USN \_ já está definida para o registro existente, nenhuma alteração é feita no registro.<br/>                                                                                           |
| Truncamento de arquivo<br/>            | O sistema de arquivos NTFS grava um novo registro de USN com a configuração do sinalizador USN motivo da redefinição de \_ \_ dados do motivo do \_ \| USN \_ razão \_ \_ informações básicas alterar o \_ \| \_ \_ truncamento de dados do motivo do USN \_ .<br/>                                                                                           |
| Terceira operação de gravação<br/>      | O sistema de arquivos NTFS não grava um novo registro USN. Como \_ \_ a substituição de dados do motivo do USN \_ já está definida para o registro existente, nenhuma alteração é feita no registro.<br/>                                                                                           |
| Fechar operação<br/>            | Se o usuário que faz alterações for o único usuário do arquivo, o sistema de arquivos NTFS gravará um novo registro de USN com a seguinte configuração de sinalizador: USN motivo de substituição de dados do motivo do USN informações básicas do motivo USN de \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ truncamento de dados do \_ arredondamento do USN \| \_ motivo \_ fechar.<br/> |



 

O diário de alterações acumula uma série de registros entre a primeira abertura e o último fechamento de um arquivo. Cada registro tem um novo sinalizador de motivo definido, indicando que ocorreu um novo tipo de alteração. A sequência de registros fornece um histórico parcial do arquivo. O registro final, criado quando o arquivo é fechado, adiciona o sinalizador de fechamento do motivo do USN \_ \_ . Esse registro representa um resumo das alterações no arquivo, mas ao contrário dos registros anteriores, não fornece nenhuma indicação da ordem das alterações.

O próximo usuário a acessar e alterar o arquivo gera um novo registro de USN com um único sinalizador de motivo.

 

 




