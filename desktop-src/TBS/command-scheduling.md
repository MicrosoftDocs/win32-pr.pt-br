---
title: Agendamento de comandos
description: Cada comando tem uma prioridade associada a ele.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756344"
---
# <a name="command-scheduling"></a>Agendamento de comandos

## <a name="command-scheduling"></a>Agendamento de comandos

Os comandos podem ser enviados para o TBS a partir de vários contextos a qualquer momento. No entanto, um TPM físico só pode processar um comando por vez e alguns comandos podem ser executados por um período de tempo significativo. Quando vários comandos estão pendentes, o TBS decide qual comando enviar ao TPM. Quando um comando é enviado, cada comando tem uma prioridade associada a ele. O TBS usa essas prioridades para determinar qual comando pendente deve ser enviado sempre que o TPM for gratuito. Os quatro níveis de prioridade são baixo, normal, alto e sistema. Os aplicativos devem usar prioridade baixa, normal ou alta. Embora comandos de alta prioridade geralmente sejam executados antes de comandos de baixa prioridade, o Agendador de comandos TBS tem uma política de envelhecimento que, eventualmente, dá prioridade muito alta aos comandos que foram bloqueados por períodos de tempo significativos.

## <a name="context-management"></a>Gerenciamento de contexto

Quando um \_ comando SaveContext do TPM ou TPM2 ContextSave é enviado com um identificador virtual para um recurso que o TBS está gerenciando, o TBS executa o comando apropriado no recurso físico e retorna o resultado para o chamador se o recurso estiver fisicamente presente no TPM. Se o recurso não estiver fisicamente presente no TPM, o pré-processamento do \_ comando TPM SaveContext ou TPM2 \_ ContextSave fará com que o recurso seja recarregado. nesse ponto, o contexto será salvo e retornado ao chamador. Se o recurso que está sendo salvo for de um tipo que é normalmente liberado automaticamente do TPM após salvar, o TBS invalida o recurso virtual após a conclusão deste comando. Quando um \_ comando TPM loadcontext ou TPM2 \_ ContextLoad é enviado para o TBS, o TBS executa o comando imediatamente. Se o comando for concluído com êxito, o TBS virtualizará o identificador de recursos e passará o fluxo de bytes do TPM resultante para o chamador. Quando um \_ comando FlushSpecific do TPM ou TPM2 \_ FlushContext é enviado com um identificador virtual para um recurso que o TBS está gerenciando, o TBS executa um \_ comando TPM FlushSpecific ou TPM2 \_ FlushContext para remover o recurso do TPM, se ele estiver fisicamente presente. Nesse caso, o TBS invalida o recurso virtual e retorna o resultado do comando FLUSH para o chamador. Se o recurso não estiver fisicamente presente no TPM, o pré-processamento do \_ comando FlushSpecific do TPM ou do TPM2 \_ FlushContext carregará o recurso que corresponde ao identificador virtual, mas ele será liberado quando o comando for realmente processado. O TBS não dá suporte ao KeyControlOwner do TPM \_ ou à funcionalidade do keepHandle da \_ operação de metacontexto do TPM, portanto, ele não fornecerá a um recurso o mesmo identificador que tinha antes do contexto ser salvo.

## <a name="other-commands"></a>Outros comandos

Comandos que não são mencionados nesta documentação são processados substituindo identificadores de chave virtual por identificadores de chave física (se necessário) e enviando-os para o TPM. Isso é feito depois de executar as operações apropriadas para garantir que os recursos que estão sendo usados estejam fisicamente presentes no TPM. Nenhum processamento especial adicional é executado. O TBS não tenta melhorar a fidelidade da virtualização, modificando os dados passados do TPM como parte de uma consulta do TPM \_ GetCapabilities ou do TPM2 \_ GetCapability. O TBS também dá suporte a comandos de presença física de TCG. O TBS age como uma passagem para comandos de presença física; nenhum processamento especial é executado pelo próprio TBS.

## <a name="cleanup"></a>Limpeza

Quando um contexto é encerrado, todos os recursos físicos e virtuais associados a ele são limpos para que não consumam mais recursos do sistema.

 

 




