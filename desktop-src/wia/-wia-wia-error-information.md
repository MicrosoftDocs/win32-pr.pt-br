---
description: as APIs de aquisição de imagem de Windows (WIA) retornam seu status de conclusão em um valor de retorno HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informações de erro WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056956"
---
# <a name="wia-error-information"></a>Informações de erro WIA

as APIs de aquisição de imagem de Windows (WIA) retornam seu status de conclusão em um valor de retorno HRESULT. Os aplicativos verificam esses valores de retorno em relação à constante de recurso \_ WIA para determinar se o erro exige a limpeza da intervenção do usuário, como um caminho de papel emperrado e relatá-los para o usuário. Além disso, todos os erros de nível de driver são registrados em detalhes no log de eventos, usando cadeias de caracteres de erro fornecidas pelo dispositivo minidriver. Para obter uma lista de códigos de erro específicos do WIA, consulte [códigos de erro](-wia-error-codes.md).

 

 



