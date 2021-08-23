---
description: O objeto address representa uma entidade que pode fazer ou receber chamadas.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objeto de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9265663692b77ad8bf7c71b5efabf6485edc747da9cbf68de387df77089305f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872360"
---
# <a name="address-object"></a>Objeto de endereço

O objeto address representa uma entidade que pode fazer ou receber chamadas. Esse objeto expõe interfaces e métodos que permitem que um aplicativo execute várias operações, como:

-   Descubra se um endereço especificado pode dar suporte a um determinado conjunto de necessidades de tipo de mídia.
-   Enumere as chamadas associadas ao endereço no momento.
-   Criar ou encaminhar chamadas.
-   Obtenha o nome do provedor de serviços associado.
-   Se um provedor de serviços de mídia existir, obtenha os ponteiros de interface que permitem a manipulação de terminal detalhada.
-   Obter e definir outras informações, como se uma mensagem está aguardando.

A maioria dos endereços está associada a um terminal, mas isso não é uniformemente o caso. Por exemplo, um TSP remoto que fornece acesso a equipamentos em um servidor terá um endereço no computador local, mas não um terminal. Um modem sem viva-voz também não tem nenhum terminal associado ao seu endereço.

Se um endereço não tiver um terminal associado, a interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) não será exposta no objeto.

O exemplo do código [selecionar um endereço](select-an-address.md) mostra o processo básico para a aquisição de um ponteiro de objeto de endereço.

Consulte [interfaces de objeto de endereço](address-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto de endereço.

 

 
