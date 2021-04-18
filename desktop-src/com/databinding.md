---
title: Associação de dados
description: Associação de dados
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105786228"
---
# <a name="databinding"></a>Associação de dados

Um novo atributo DataBinding foi adicionado para permitir que as propriedades se diferenciem entre as alterações de comunicação somente quando o foco deixa o controle ou durante todas as notificações de alteração de propriedade.

O novo atributo, conhecido como ImmediateBind, permite que os controles diferenciem dois tipos diferentes de propriedades vinculáveis. Um tipo de propriedade vinculável precisa notificar todas as alterações no banco de dados, por exemplo, com um controle caixa de seleção em que cada alteração precisa ser enviada para o banco de dados subjacente, embora o controle não tenha perdido o foco. No entanto, os controles como uma ListBox só querem ter a alteração de uma propriedade notificada para o banco de dados quando o controle perde o foco, pois o usuário pode ter alterado a seleção realçada com as teclas de direção antes de localizar a configuração desejada, para que a notificação de alteração seja enviada ao banco de dados sempre que o usuário atingir a tecla de seta seria inaceitável. A nova propriedade de ligação imediata permite que as propriedades vinculáveis individuais em um formulário tenham esse comportamento especificado, quando esse bit for definido, todas as alterações serão notificadas.

O novo bit ImmediateBind é mapeado para o novo VARFLAG \_ FIMMEDIATEBIND (0x80) e os bits FUNCFLAG FIMMEDIATEBIND \_ (0x80) nas enumerações VARFLAGS e FUNCFLAGS para a interface [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , permitindo que os atributos de propriedades sejam inspecionados.

 

 