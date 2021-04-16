---
title: Alterando a sincronização do Sequencer
description: Alterando a sincronização do Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105750210"
---
# <a name="changing-sequencer-synchronization"></a>Alterando a sincronização do Sequencer

> [!NOTE]
> Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.  Neste documento, há referências à palavra ' escravo '. O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa palavra-chave é usada, pois é atualmente a palavra usada no software. Para fins de consistência, este documento contém esta palavra. Quando esta palavra for removida do software, corrigiremos este documento para estar em alinhamento.

Para alterar o modo de sincronização de um dispositivo de sequenciador, use a mensagem de comando do [**MCI \_ set**](mci-set.md) com os \_ \_ \_ sinalizadores subordinados do MCI Set Master e MCI \_ \_ set \_ slave. Dois membros na estrutura [**MCI \_ \_ set \_ parms**](mci-seq-set-parms.md) , **dwMaster** e **dwSlave**, são usados para especificar os modos de sincronização mestre e subordinado.

O modo de sincronização mestre controla as informações de sincronização enviadas pelo Sequencer para uma porta de saída. A seguir estão as constantes para o membro **dwMaster** e seus modos de sincronização mestre correspondentes.



| Constante        | Modo de sincronização                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ Seq \_ Midi  | Sincronização de MIDI. Envie informações de tempo para a porta de saída usando mensagens de relógio de temporização de MIDI.   |
| MCI \_ Seq \_ SMPTE | Sincronização de SMPTE. Envie informações de tempo para a porta de saída usando mensagens de quadro do trimestre MIDI. |
| \_Seq MCI \_ None  | Sem sincronização. Não enviar informações de tempo.                                                  |



 

O modo de sincronização subordinada controla onde o Sequencer obtém suas informações de tempo para reproduzir um arquivo MIDI. A seguir estão as constantes para o membro **dwSlave** e seus modos de sincronização subordinada correspondentes.



| Constante        | Modo de sincronização                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_arquivo Seq \_ MCI  | Sincronização de arquivos. Obter informações de tempo do arquivo MIDI.                                                                                       |
| MCI \_ Seq \_ Midi  | Sincronização de MIDI. Obtenha informações de tempo da porta de entrada usando mensagens de relógio de tempo de MIDI.                                                     |
| MCI \_ Seq \_ SMPTE | Sincronização de SMPTE. Obtenha informações de tempo da porta de entrada usando mensagens de quadro do trimestre MIDI.                                                   |
| \_Seq MCI \_ None  | Sem sincronização. Obtenha informações de tempo somente de comandos MCI e ignore informações de tempo (como alterações de tempo) que estão no arquivo MIDI. |



 

> [!Note]  
> Atualmente, para a sincronização mestre, o sequenciador MIDI MCI só dá suporte ao modo sem sincronização (MCI \_ Seq \_ nenhum). Para a sincronização subordinada, ele dá suporte apenas ao modo de sincronização de arquivo ( \_ arquivo MCI Seq \_ ) e ao modo sem sincronização (MCI \_ Seq \_ nenhum).

 

 

 




