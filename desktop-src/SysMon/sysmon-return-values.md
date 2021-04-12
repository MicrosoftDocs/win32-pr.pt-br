---
title: Valores de retorno de SYSMON
description: A seguir está uma lista de valores de retorno do monitor do sistema que são definidos em Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366429"
---
# <a name="sysmon-return-values"></a>Valores de retorno de SYSMON

A seguir está uma lista de valores de retorno do monitor do sistema que são definidos em Smonmsg. h.



| Valor retornado                                       | Descrição                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ status \_ DUPL \_ \_ caminho do contador (0xC0001388)     | A coleção de contadores já contém o contador especificado.                                                                                                                                                                               |
| \_Status \_ do SMON no \_ \_ objeto SYSMON (0xC0001389)      | As configurações não contêm nenhum objeto HTML do monitor de sistema completo.                                                                                                                                                                        |
| SMON \_ o \_ status \_ \_ de poucas amostras (0xC000138A)       | O arquivo de log especificado contém menos de dois exemplos de dados.                                                                                                                                                                                 |
| \_ \_ \_ \_ \_ Limite de tamanho do arquivo de log de status SMON (0xC000138B)  | O arquivo de log especificado excede os limites de tamanho do controle do monitor do sistema. Se um arquivo de log estiver selecionado no momento, selecione atividade atual como a fonte de dados para descarregar o arquivo de log atual e, em seguida, selecione novamente o arquivo de log especificado. |
| \_ \_ \_ \_ \_ Fonte de dados do arquivo de log de status SMON (0xC000138C) | Para adicionar um novo arquivo de log à fonte de dados, o tipo de fonte de dados deve ser alterado para um tipo diferente de sysmonLogFiles.                                                                                                                          |
| SMON \_ status \_ DUPL \_ log \_ File \_ Path (0xC000138D)   | A coleção de arquivos de log já contém o arquivo de log especificado.                                                                                                                                                                             |



 

Para obter uma descrição de valores de retorno adicionais retornados pelo monitor do sistema, consulte códigos de [erro do sistema](/windows/desktop/Debug/system-error-codes) e [códigos de erro auxiliares de dados de desempenho](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 