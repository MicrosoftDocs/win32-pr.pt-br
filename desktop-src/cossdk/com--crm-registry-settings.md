---
description: Várias configurações do registro estão disponíveis para modificar o comportamento do CRM para auxiliar na solução de problemas e no desenvolvimento.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Configurações do registro do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826264"
---
# <a name="com-crm-registry-settings"></a>Configurações do registro do CRM do COM+

Várias configurações do registro estão disponíveis para modificar o comportamento do CRM para auxiliar na solução de problemas e no desenvolvimento. Todas essas configurações do registro, que são listadas e descritas na tabela a seguir, são opcionais; nenhum é necessário para a operação normal do CRM.

Todas as configurações do registro do CRM estão em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ com3 \\ CRM**. Crie a chave de **CRM** sob a chave **com3** se ela ainda não estiver lá.



| Configurações do registro do CRM                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | Valor do REG \_ DWORD. Definir esse valor como qualquer coisa diferente de zero habilita a depuração de mensagens de rastreamento em avisos ou erros. Essas mensagens podem ser vistas na janela de saída do depurador. Esse valor deve ser definido apenas para desenvolvimento e não durante a implantação normal. Esse valor é lido quando qualquer aplicativo do servidor CRM é iniciado.<br/>                                                                                                                                                                                                                                                   |
| **IgnoreCompensatorErrors**<br/> | Valor do REG \_ DWORD. Definir esse valor como algo diferente de zero permite que a infraestrutura de CRM ignore todos os erros retornados de compensadores de CRM. Se a recuperação estiver falhando devido a um erro de um compensador de CRM, a definição desse valor permitirá que a recuperação seja concluída. Esse valor é lido quando qualquer aplicativo do servidor CRM é iniciado.<br/>                                                                                                                                                                                                                                           |
| **CheckpointIntervalInSec**<br/> | Valor do REG \_ DWORD. Esse é o intervalo de ponto de verificação em segundos. O intervalo de ponto de verificação padrão é de 30 segundos. Os pontos de verificação são usados para recuperar espaço do arquivo de log do CRM. Aumentar o intervalo de ponto de verificação pode aumentar o desempenho, mas às custas do maior tempo de recuperação e de um arquivo de log de CRM maior. Esse valor é lido quando qualquer aplicativo do servidor CRM é iniciado.<br/>                                                                                                                                                                                                  |
| **InitialLogFileSizeInKB**<br/>  | Valor do REG \_ DWORD. Esse é o tamanho inicial do arquivo de log do CRM em kilobytes. O tamanho padrão do arquivo de log do CRM é 1024 KB (1 MB). O arquivo de log do CRM é expandido automaticamente para atender à carga da transação imposta, mas se cargas pesadas forem previstas, poderá ser necessário aumentar esse valor. Esse valor é lido quando qualquer aplicativo de servidor do COM+ habilitado para CRM é iniciado, mas se o arquivo de log do CRM já existir para um aplicativo do servidor CRM, esse valor será ignorado para esse aplicativo de servidor.<br/>                                                                               |
| **RecoveryTraceEnabled**<br/>    | Valor do REG \_ DWORD. Definir esse valor como algo diferente de zero habilita um rastreamento de recuperação. O rastreamento de recuperação é um arquivo de texto que tem o mesmo nome que o arquivo de log do CRM e a seguinte extensão adicional: .recoverytrace.txt. <br/> Esse arquivo está localizado no mesmo diretório que o arquivo de log do CRM. O rastreamento de recuperação fornece um rastreamento de atividade de CRM durante a recuperação, que pode ser usado para diagnóstico de problemas. Esse valor é lido quando qualquer aplicativo do servidor CRM é iniciado. No entanto, um arquivo de rastreamento de recuperação exclusivo é produzido para cada aplicativo do servidor CRM.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




