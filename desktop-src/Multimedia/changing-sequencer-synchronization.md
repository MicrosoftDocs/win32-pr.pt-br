---
title: Alterando a sincronização do sequencer
description: Alterando a sincronização do sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f7f31544b7b9ceb00109551718b9984dd2aa506557848e0d63e77724c4be32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526416"
---
# <a name="changing-sequencer-synchronization"></a>Alterando a sincronização do sequencer

> [!NOTE]
> Comunicação sem preconceitos A Microsoft dá suporte a um ambiente diversificado e inclusões.  Neste documento, há referências à palavra 'slave'. O Guia de Estilo da Microsoft [para Bias-Free Comunicações](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa redação é usada, pois atualmente é a palavra usada no software. Para consistência, este documento contém essa palavra. Quando essa palavra for removida do software, corrigiremos este documento para estar em alinhamento.

Para alterar o modo de sincronização de um dispositivo sequenciador, use a mensagem de comando [**MCI \_ SET**](mci-set.md) com os sinalizadores MCI SEQ SET MASTER e \_ \_ \_ MCI \_ SEQ SET \_ \_ SLAVE. Dois membros na estrutura [**MCI \_ SEQ SET \_ \_ PARMS,**](mci-seq-set-parms.md) **dwMaster** e **dwMinee**, são usados para especificar os modos de sincronização mestre e subordinado.

O modo de sincronização mestre controla as informações de sincronização enviadas pelo sequenciador para uma porta de saída. A seguir estão as constantes para o **membro dwMaster** e seus modos de sincronização mestre correspondentes.



| Constante        | Modo de sincronização                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ MIDI  | Sincronização MIDI. Enviar informações de tempo para a porta de saída usando mensagens de relógio MIDI.   |
| MCI \_ SEQ \_ SMPTE | Sincronização SMPTE. Enviar informações de tempo para a porta de saída usando mensagens de trimestre MIDI. |
| MCI \_ SEQ \_ NONE  | Sem sincronização. Não envie nenhuma informação de tempo.                                                  |



 

O modo de sincronização subordinada controla onde o sequenciador obtém suas informações de tempo para reproduzir um arquivo MIDI. A seguir estão as constantes para o **membro dwGatee** e seus modos de sincronização subordinados correspondentes.



| Constante        | Modo de sincronização                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ARQUIVO SEQ da \_ MCI \_  | Sincronização de arquivos. Obter informações de tempo do arquivo MIDI.                                                                                       |
| MCI \_ SEQ \_ MIDI  | Sincronização MIDI. Obter informações de tempo da porta de entrada usando mensagens de relógio MIDI.                                                     |
| MCI \_ SEQ \_ SMPTE | Sincronização SMPTE. Obter informações de tempo da porta de entrada usando mensagens de trimestre MIDI.                                                   |
| MCI \_ SEQ \_ NONE  | Sem sincronização. Obter informações de tempo somente de comandos MCI e ignorar informações de tempo (como alterações de tempo) que estão no arquivo MIDI. |



 

> [!Note]  
> Atualmente, para sincronização mestre, o sequenciador MCI MIDI dá suporte apenas ao modo Sem Sincronização (MCI \_ SEQ \_ NONE). Para sincronização subordinada, ele dá suporte apenas ao modo de Sincronização de Arquivos (MCI SEQ FILE) e ao modo Sem Sincronização \_ \_ (MCI \_ SEQ \_ NONE).

 

 

 




