---
description: Quando um thread está se comunicando ativamente com um dispositivo WIA (aquisição de imagem do Windows) (por exemplo, transferindo dados ou gravando Propriedades do dispositivo) WIA &\# 0034; bloqueios&\# 0034; o dispositivo.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Comunicando-se com um dispositivo WIA em vários threads ou aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169543"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Comunicando-se com um dispositivo WIA em vários threads ou aplicativos

Quando um thread está se comunicando ativamente com um dispositivo WIA (aquisição de imagem do Windows) (por exemplo, transferindo dados ou gravando Propriedades do dispositivo), o WIA "bloqueia" o dispositivo. Quando um dispositivo está bloqueado, nenhum outro thread ou processo pode se comunicar ativamente com esse dispositivo.

O WIA não proíbe que vários threads ou processos mantenham conexões com um único dispositivo. Ou seja, um dispositivo está bloqueado somente durante a comunicação real e dois ou mais aplicativos podem ter um único dispositivo selecionado simultaneamente.

O WIA cria uma árvore de itens separada sempre que qualquer thread ou aplicativo chama [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) ou [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) para criar uma instância desse dispositivo. O WIA mantém informações de estado separadas para cada árvore de itens. Por exemplo, se um thread criar duas instâncias de um verificador específico, ele poderá definir resoluções de verificação diferentes para as duas instâncias. Quando [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) é chamado em uma determinada instância, o WIA carrega as propriedades associadas a essa instância para o dispositivo antes que a verificação real ocorra. Isso não afeta o estado da outra instância do dispositivo.

Se um thread tiver um dispositivo bloqueado (está ativamente se comunicando com esse dispositivo) e outro thread tentar chamar um método que se comunica ativamente com o dispositivo, o método retornará um erro de \_ erro de WIA \_ ocupado.

Normalmente, a leitura e a gravação das propriedades do dispositivo leva pouco tempo que essas operações raramente causam um conflito. A transferência de dados, no entanto, geralmente leva mais tempo e, portanto, é mais provável que você crie conflitos de acesso ao dispositivo. É uma programação de som para evitar operações de dispositivo demoradas (transferências de dados) simultaneamente em threads separados dentro de um aplicativo.

Um aplicativo nunca deve supor que é o único aplicativo que está se comunicando com um dispositivo WIA quando ele é iniciado.

 

 



