---
title: Criando discos com várias sessões
description: O IMAPi é capaz de criar discos de dados de várias sessões. Há algumas considerações a serem consideradas ao criar um disco de várias sessões.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159653"
---
# <a name="creating-discs-with-multiple-sessions"></a>Criando discos com várias sessões

O IMAPi é capaz de criar discos de dados de várias sessões. Há algumas considerações a serem consideradas ao criar um disco de várias sessões.

O método [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se há um disco IMAPI com várias sessões na unidade ativa na configuração. Nesse caso, o IMAPi entra em modo de várias sessões automaticamente. O uso de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) após o modo de várias sessões ter sido estabelecido faz com que o IMAPI retorne ao modo de sessão única. Isso significa que um disco em branco é necessário para uma gravação [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) . Se o disco estiver no modo de várias sessões, o mesmo disco deverá estar no gravador ativo ou um código de erro de IMAPi \_ E \_ WRONGDISC será retornado.

A seleção de um gravador no formato Joliet faz com que o IMAPi Leia as informações do disco atualmente instalado. Se o disco for um disco de IMAPi Joliet anterior que tem espaço para outra sessão, o IMAPi se definirá automaticamente para o modo de várias sessões. Esse disco deve estar presente no gravador ativo ao chamar [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

Fechar a primeira sessão em um disco requer 21 MB. Cada sessão adicional requer 11 MB para ser fechada.

 

 




