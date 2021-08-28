---
title: Propriedades de anotação que têm winEvents correspondentes
description: Tenha cuidado ao substituindo propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como Estado, Valor e, para alguns controles, as propriedades Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753a17498daf9966ed1c3dfa98dc64fbdb2290011842c4fe9c194f50bf408ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098506"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Propriedades de anotação que têm winEvents correspondentes

Tenha cuidado ao substituindo propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como [**State**](state-property.md), [**Value**](value-property.md)e, para alguns controles, as propriedades [**Name).**](name-property.md)

Em muitos casos, especialmente para controles USER e ComCtl, o WinEvent sinalizando uma alteração de propriedade é enviado antes que o proprietário do controle seja notificado (normalmente por meio [de WM \_ NOTIFY](../controls/wm-notify.md)). Atualizar a propriedade usando [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) no manipulador WM NOTIFY será muito tarde; os clientes que usam o gancho no contexto já \_ acessarão o valor antigo.

Você pode lidar com esses tipos de propriedades usando objetos de servidor de retorno de chamada (usando [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); no entanto, o servidor não pode usar nenhum estado que seja atualizado no manipulador WM NOTIFY porque esse \_ manipulador ainda não terá sido chamado. Por exemplo, em vez de usar uma variável de valor atual armazenada em cache que é atualizada no manipulador WM NOTIFY e estará des date, o objeto de retorno de chamada \_ [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve enviar uma mensagem diretamente para o controle para obter seu valor atual verdadeiro para gerar a propriedade necessária.

 

 