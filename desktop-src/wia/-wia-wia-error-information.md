---
description: As APIs de aquisição de imagem do Windows (WIA) retornam seu status de conclusão em um valor de retorno HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informações de erro WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780397"
---
# <a name="wia-error-information"></a>Informações de erro WIA

As APIs de aquisição de imagem do Windows (WIA) retornam seu status de conclusão em um valor de retorno HRESULT. Os aplicativos verificam esses valores de retorno em relação à constante de recurso \_ WIA para determinar se o erro exige a limpeza da intervenção do usuário, como um caminho de papel emperrado e relatá-los para o usuário. Além disso, todos os erros de nível de driver são registrados em detalhes no log de eventos, usando cadeias de caracteres de erro fornecidas pelo dispositivo minidriver. Para obter uma lista de códigos de erro específicos do WIA, consulte [códigos de erro](-wia-error-codes.md).

 

 



