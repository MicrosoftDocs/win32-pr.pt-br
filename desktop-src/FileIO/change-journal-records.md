---
description: À medida que arquivos, diretórios e outros objetos do sistema de arquivos NTFS são adicionados, excluídos e modificados, o sistema de arquivos NTFS entra em registros de diário de alteração em fluxos, um para cada volume no computador.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Alterar registros de diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313dde6a71b36ed046a7086d39ce8e1a86b909cc7c815f295bb8a45c82ab92f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765986"
---
# <a name="change-journal-records"></a>Alterar registros de diário

À medida que arquivos, diretórios e outros objetos do sistema de arquivos NTFS são adicionados, excluídos e modificados, o sistema de arquivos NTFS entra em registros de diário de alteração em fluxos, um para cada volume no computador. Cada registro indica o tipo de alteração e o objeto alterado. O deslocamento do início do fluxo para um registro específico é chamado de USN (número de sequência de atualização) para o registro específico. Novos registros são anexados ao final do fluxo.

O sistema de arquivos NTFS pode excluir registros antigos para conservar espaço. Se os registros necessários tiverem sido excluídos, o serviço de indexação será recuperado re indexando o volume, como acontece quando não há nenhum diário de alteração.

O diário de alteração registra apenas o fato de uma alteração em um arquivo e o motivo da alteração (por exemplo, operações de gravação, truncamento, alongamento, exclusão e assim por diante). Ele não registra informações suficientes para permitir a reversão da alteração.

Além disso, várias alterações no mesmo arquivo podem resultar em apenas um sinalizador de motivo sendo adicionado ao registro atual. Se o mesmo tipo de alteração ocorrer mais de uma vez, o sistema de arquivos NTFS não gravará um novo registro para as alterações após o primeiro. Por exemplo, várias operações de gravação sem operações de fechamento e reabertura intermediárias resultam em apenas um registro de alteração com o sinalizador motivo USN \_ REASON \_ DATA \_ OVERWRITE definido.

Para ilustrar como o diário de alterações funciona, suponha que um usuário acesse um arquivo na seguinte ordem:

1.  Grava no arquivo.
2.  Define o carimbo de data/hora do arquivo.
3.  Grava no arquivo.
4.  Trunca o arquivo.
5.  Grava no arquivo.
6.  Fecha o arquivo.

Nesse caso, o sistema de arquivos NTFS toma as seguintes ações no diário de alterações (em que \| indica uma operação OR bit a bit).



| Evento                                 | Ação do sistema de arquivos NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operação de gravação inicial<br/>    | O sistema de arquivos NTFS grava um novo registro USN com o sinalizador DE motivo SOBRE SUBSTITUIR DADOS DO MOTIVO DA USN \_ \_ \_ definido. Para obter mais informações sobre possíveis sinalizadores de motivo, consulte a [**estrutura USN \_ RECORD.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)<br/>                                                     |
| Configuração do carimbo de data/hora do arquivo<br/> | O sistema de arquivos NTFS grava um novo registro USN com o sinalizador definindo USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ \_ \_ \_ CHANGE.<br/>                                                                                                                            |
| Segunda operação de gravação<br/>     | O sistema de arquivos NTFS não grava um novo registro USN. Como USN \_ REASON \_ DATA OVERWRITE já está definido para o registro existente, nenhuma \_ alteração é feita no registro.<br/>                                                                                           |
| Truncamento de arquivo<br/>            | O sistema de arquivos NTFS grava um novo registro USN com o sinalizador definindo USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ \_ CHANGE \_ \_ \| USN REASON DATA \_ \_ \_ TRUNCATION.<br/>                                                                                           |
| Terceira operação de gravação<br/>      | O sistema de arquivos NTFS não grava um novo registro USN. Como USN \_ REASON \_ DATA OVERWRITE já está definido para o registro existente, nenhuma \_ alteração é feita no registro.<br/>                                                                                           |
| Operação de fechamento<br/>            | Se o usuário que faz alterações for o único usuário do arquivo, o sistema de arquivos NTFS gravará um novo registro USN com a seguinte configuração de sinalizador: USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ CHANGE \_ \_ \_ \| USN REASON DATA \_ \_ \_ \| TRUNCATION USN REASON \_ \_ CLOSE.<br/> |



 

O diário de alteração acumula uma série de registros entre a primeira abertura e o último fechamento de um arquivo. Cada registro tem um novo sinalizador de motivo definido, indicando que ocorreu um novo tipo de alteração. A sequência de registros fornece um histórico parcial do arquivo. O registro final, criado quando o arquivo é fechado, adiciona o sinalizador USN \_ REASON \_ CLOSE. Esse registro representa um resumo das alterações no arquivo, mas, ao contrário dos registros anteriores, não fornece nenhuma indicação da ordem das alterações.

O próximo usuário a acessar e alterar o arquivo gera um novo registro USN com um único sinalizador de motivo.

 

 




