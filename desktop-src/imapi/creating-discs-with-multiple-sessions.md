---
title: Criando discos com várias sessões
description: O IMAPI é capaz de criar discos de dados de várias sessões. Há algumas considerações a serem consideradas ao criar um disco de várias sessões.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b108a6b7b07d6d82230362899da26e7264e62a460c197338e223f0e95078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977116"
---
# <a name="creating-discs-with-multiple-sessions"></a>Criando discos com várias sessões

O IMAPI é capaz de criar discos de dados de várias sessões. Há algumas considerações a serem consideradas ao criar um disco de várias sessões.

O [**método IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se há um disco de várias sessões IMAPI na unidade ativa após a configuração. Nesse caso, o IMAPI entra no modo de várias sessões automaticamente. Usar [**ClearFormatContent após**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) o modo de várias sessões tiver sido estabelecido faz com que o IMAPI retorne ao modo de sessão única. Isso significa que um disco em branco é necessário para uma [**gravação de RecordDisc.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) Se o disco estiver no modo de várias sessões, o mesmo disco deverá estar no gravador ativo ou um código de erro de IMAPI \_ E \_ WRONGDISC será retornado.

Selecionar um gravador enquanto estiver no formato Devt faz com que o IMAPI leia informações do disco instalado no momento. Se o disco for um disco IMAPI Que tenha espaço para outra sessão, o IMAPI automaticamente se define para o modo de várias sessões. Esse disco deve estar presente no gravador ativo ao chamar [**RecordDisc.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)

Fechar a primeira sessão em um disco requer 21 MB. Cada sessão adicional requer 11 MB para ser fechado.

 

 




