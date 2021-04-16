---
description: A função phoneClose fecha o dispositivo de telefone especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Fechando o dispositivo de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502049"
---
# <a name="closing-the-phone-device"></a>Fechando o dispositivo de telefone

A função [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) fecha o dispositivo de telefone especificado. O dispositivo de telefone também pode ser fechado à força após o usuário ter modificado a configuração desse telefone ou de seu driver. Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá forçar o fechamento do dispositivo telefônico.

Essas mensagens também podem ser enviadas não solicitadas como resultado do dispositivo telefônico que está sendo recuperado de alguma outra maneira. Portanto, um aplicativo deve estar preparado para lidar com mensagens [**de \_ fechamento de telefone**](phone-close.md) não solicitadas. No momento em que o dispositivo de telefone é fechado, todas as respostas assíncronas pendentes relacionadas ao dispositivo são suprimidas.

 

 



