---
description: O WIA fornece uma camada de compatibilidade DOLS que permite que aplicativos com conhecimento de ECHO se comuniquem com Windows WIA (Aquisição de Imagem).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidade com o LTD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056976"
---
# <a name="twain-compatibility"></a>Compatibilidade com o LTD

O WIA fornece uma camada de compatibilidade DOLS que permite que aplicativos com conhecimento de ECHO se comuniquem com Windows WIA (Aquisição de Imagem). Os aplicativos com notação AODL não têm acesso completo à funcionalidade wia. Por exemplo, um aplicativo não pode suprimir a interface do usuário usando a camada de compatibilidade DOLS.

Os dispositivos WIA aparecem duas vezes para um aplicativo que está ciente do WIA e DOLS: uma vez por meio da comunicação WIA normal e uma vez por meio da camada de compatibilidade DOIS. Para evitar a listagem de um dispositivo WIA duas vezes, um aplicativo que esteja ciente do WIA e DOIS deve filtrar os dispositivos WIA que vêm por meio da camada de compatibilidade DOIS. Todos os dispositivos WIA que vêm por meio da camada de compatibilidade DOLS têm "WIA-" como prefixo, portanto, é fácil filtrá-los.

 

 



