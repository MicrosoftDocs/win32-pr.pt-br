---
description: O WIA fornece uma camada de compatibilidade TWAIN que permite que aplicativos com reconhecimento de TWAIN se comuniquem com dispositivos WIA (aquisição de imagens do Windows).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidade com TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760998"
---
# <a name="twain-compatibility"></a>Compatibilidade com TWAIN

O WIA fornece uma camada de compatibilidade TWAIN que permite que aplicativos com reconhecimento de TWAIN se comuniquem com dispositivos WIA (aquisição de imagens do Windows). Os aplicativos com reconhecimento de TWAIN não têm acesso completo à funcionalidade WIA. Por exemplo, um aplicativo não pode suprimir a interface do usuário usando a camada de compatibilidade TWAIN.

Os dispositivos WIA aparecem duas vezes para um aplicativo que reconhece o WIA e o TWAIN: uma vez por meio da comunicação de WIA normal e uma vez por meio da camada de compatibilidade TWAIN. Para evitar a listagem de um dispositivo WIA duas vezes, um aplicativo que reconhece o WIA e o TWAIN deve filtrar os dispositivos WIA que vêm pela camada de compatibilidade TWAIN. Todos os dispositivos WIA que vêm pela camada de compatibilidade TWAIN têm "WIA-" como um prefixo, portanto, é fácil filtrá-los.

 

 



