---
description: Monitor de Rede chama a função Formatproperties para formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementando Formatproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7b927f15ccb2c216e345b37bc87593e33339671f906e28d33759ca9db0abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778966"
---
# <a name="implementing-formatproperties"></a>Implementando Formatproperties

Monitor de Rede chama a função [**formatproperties**](formatproperties.md) para formatar os dados que são exibidos no painel de detalhes da interface do usuário do monitor de rede. Normalmente, **formatproperties** é chamado para formatar a linha de Resumo de um protocolo e, em seguida, Formatar todas as instâncias de Propriedade do protocolo dentro de um quadro. No entanto, Monitor de Rede não identifica o número de vezes que **formatproperties** é chamado para um analisador específico.

Ao chamar [**formatproperties**](formatproperties.md), o monitor de rede fornece uma estrutura [**PROPERTYINST**](propertyinst.md) para cada propriedade exibida. A estrutura **PROPERTYINST** fornece informações sobre os dados a serem exibidos, incluindo um ponteiro para a estrutura [**PROPERTYINFO**](propertyinfo.md) que especifica a função a ser usada para formatar a propriedade de dados exibida.

> [!Note]  
> Uma estrutura [**PROPERTYINFO**](propertyinfo.md) é especificada ao adicionar uma propriedade ao [*banco de dados de propriedade*](p.md) do analisador.

 

Monitor de Rede identifica a função de formato a ser chamada para cada instância de propriedade. O membro **InstanceData** da estrutura [**PROPERTYINFO**](propertyinfo.md) pode especificar o seguinte:

-   A função [**FormatPropertyInstance**](formatpropertyinstance.md) para usar o [*formatador genérico*](g.md) que o monitor de rede fornece.

    – ou –

-   O nome de uma função de formato personalizado que o analisador fornece.

As funções de formato [**FormatPropertyInstance**](formatpropertyinstance.md) e personalizado retornam os dados formatados que são exibidos no painel de detalhes da interface do usuário do monitor de rede.

A ilustração a seguir mostra como Monitor de Rede identifica a função a ser chamada para cada instância de propriedade.

![como o monitor de rede identifica a função a ser chamada](images/formatprop1.png)

O procedimento a seguir identifica as etapas necessárias para implementar [**formatproperties**](formatproperties.md).

**Para implementar Formatproperties**

-   Usando uma estrutura de loop, chame a função Format para cada estrutura [**PROPERTYINST**](propertyinst.md) que é passada para o analisador no parâmetro *LpPropInst* da função [**formatproperties**](formatproperties.md) .

A seguir está uma implementação básica de [**formatproperties**](formatproperties.md).

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



