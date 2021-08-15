---
title: Valores de retorno do SYSMON
description: Veja a seguir uma lista dos valores de retorno do Monitor do Sistema definidos em Smonmsg.h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce526a64132cef51338a83b387aa8e9bfd58ce0ef0b99a1fb7db0dce4c15ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956442"
---
# <a name="sysmon-return-values"></a>Valores de retorno do SYSMON

Veja a seguir uma lista dos valores de retorno do Monitor do Sistema definidos em Smonmsg.h.



| Valor retornado                                       | Descrição                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAMINHO DO CONTADOR DUPL DE STATUS DO SMON \_ \_ \_ \_ (0XC0001388)     | A coleção de contadores já contém o contador especificado.                                                                                                                                                                               |
| STATUS SMON \_ \_ NENHUM OBJETO \_ SYSMON \_ (0xC0001389)      | As configurações não contêm nenhum objeto HTML completo do Monitor do Sistema.                                                                                                                                                                        |
| SMON \_ STATUS TOO FEW \_ \_ \_ SAMPLES (0XC000138A)       | O arquivo de log especificado contém menos de dois exemplos de dados.                                                                                                                                                                                 |
| LIMITE DE TAMANHO DO \_ ARQUIVO DE LOG DE STATUS \_ \_ \_ \_ SMON (0XC000138B)  | O arquivo de log especificado excede os limites de tamanho do controle Monitor do Sistema. Se um arquivo de log estiver selecionado no momento, selecione a atividade atual como a fonte de dados para descarregar o arquivo de log atual e, em seguida, selecione o arquivo de log especificado. |
| FONTE DE DADOS DO ARQUIVO DE LOG DE STATUS DO SMON \_ \_ \_ \_ \_ (0xC000138C) | Para adicionar um novo arquivo de log à fonte de dados, o tipo de fonte de dados deve ser alterado para um tipo diferente de sysmonLogFiles.                                                                                                                          |
| CAMINHO DO ARQUIVO DE LOG DUPL DE STATUS DO SMON \_ \_ \_ \_ \_ (0xC000138D)   | A coleção de arquivos de log já contém o arquivo de log especificado.                                                                                                                                                                             |



 

Para obter uma descrição dos valores retornados adicionais retornados pelo Monitor do Sistema, [consulte](/windows/desktop/Debug/system-error-codes) Códigos de Erro do Sistema e Códigos de Erro do Auxiliar de Dados [de Desempenho](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 