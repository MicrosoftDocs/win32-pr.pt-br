---
description: Este tópico fornece um procedimento para executar a gravação controlada por controle de fluxos de áudio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Registro de Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828674"
---
# <a name="track-controlled-record"></a>Registro de Track-Controlled

Este tópico fornece um procedimento para executar a gravação controlada por controle de fluxos de áudio.

**Para executar a gravação controlada pelo controle de fluxos de áudio**

1.  Selecione Arquivo faixas terminais em fluxos.
2.  Crie o terminal de registro de arquivo.
3.  Defina o nome do arquivo.
4.  Enumere os fluxos na chamada TAPI. Para essas etapas, consulte o procedimento a seguir.
5.  Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de registro de arquivo para iniciar a gravação de fluxo.

**Para enumerar fluxos na chamada TAPI**

1.  Crie uma faixa do mesmo tipo e direção de áudio que o fluxo.
2.  Defina as propriedades da faixa para o formato de áudio. Se não estiver definido, o formato será o mesmo que o formato de fluxos.
3.  Selecione a faixa no fluxo.

Se uma faixa for selecionada em vários fluxos, isso implica misturar fluxos.

 

 



