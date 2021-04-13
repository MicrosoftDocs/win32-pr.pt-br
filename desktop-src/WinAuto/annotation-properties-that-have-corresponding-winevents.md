---
title: Propriedades de anotação que têm WinEvents correspondente
description: Tenha cuidado ao substituir as propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como estado, valor e, para alguns controles, as propriedades de nome).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366262"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Propriedades de anotação que têm WinEvents correspondente

Tenha cuidado ao substituir as propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como [**estado**](state-property.md), [**valor**](value-property.md)e, para alguns controles, as propriedades de [**nome**](name-property.md) ).

Em muitos casos, especialmente para controles USER e ComCtl, o WinEvent sinalizando uma alteração de propriedade é enviado antes que o proprietário do controle seja notificado (normalmente via [ \_ notificação do WM](../controls/wm-notify.md)). Atualizar a propriedade usando [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) no manipulador de \_ notificação do WM será muito tarde; os clientes que usam a conexão no contexto já terão acessado o valor antigo.

Você pode lidar com esses tipos de propriedades usando objetos de servidor de chamada de retorno (usando [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); no entanto, o servidor não pode usar nenhum estado que seja atualizado no manipulador de notificação do WM \_ , pois esse manipulador ainda não terá sido chamado. Por exemplo, em vez de usar uma variável de valor atual armazenada em cache que é atualizada no manipulador de notificação do WM \_ e estará desatualizada, o objeto de retorno de chamada [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve enviar uma mensagem diretamente para o controle para obter o valor atual real para gerar a propriedade necessária.

 

 