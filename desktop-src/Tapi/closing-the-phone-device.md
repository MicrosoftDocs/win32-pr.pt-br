---
description: A função phoneClose fecha o dispositivo de telefone especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Fechando o Telefone dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7e80f3a3869df8ff508d5f4b8d9cb05f493ea0bda4e8ff0ca619d46618e7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869447"
---
# <a name="closing-the-phone-device"></a>Fechando o Telefone dispositivo

A [**função phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) fecha o dispositivo de telefone especificado. O dispositivo de telefone também pode ser fechado à força depois que o usuário tiver modificado a configuração desse telefone ou seu driver. Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo do aplicativo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá fechar o dispositivo de telefone à força.

Essas mensagens também podem ser enviadas não solicitadas como resultado da recuperação do dispositivo de telefone de alguma outra maneira. Portanto, um aplicativo deve estar preparado para lidar com mensagens [**PHONE \_ CLOSE não**](phone-close.md) solicitadas. No momento em que o dispositivo de telefone é fechado, todas as respostas assíncronas pendentes referentes a esse dispositivo são suprimidas.

 

 



