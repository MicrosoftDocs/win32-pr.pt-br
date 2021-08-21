---
description: Monitor de Rede ou a DLL do analisador podem formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formatar os dados exibidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d843214804e50d6baa7bd60f49da170dbe561029e0643c5a57c8677da3735936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982462"
---
# <a name="formatting-displayed-data"></a>Formatar os dados exibidos

Monitor de Rede ou a DLL do analisador podem formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.

O Monitor de Rede fornece um formatador genérico que fornece os serviços básicos necessários para exibir a maioria dos tipos de dados existentes em um protocolo. No entanto, o formatador genérico não oferece suporte a todos os tipos de dados. Por exemplo, o formatador genérico não oferece suporte ao seguinte:

-   Vários tipos de endereço.
-   Nomes amigáveis de origem e de destino.
-   Identificadores de objeto.
-   Tipos de dados inteiros grandes.
-   Tipos de dados inteiros pequenos de comprimento variável.

O exemplo a seguir identifica duas cadeias de caracteres formatadas para a propriedade de ID de privilégio.

-   A primeira linha de código mostra a saída do formatador genérico. A saída é baseada no tipo de dados.
-   A segunda linha de código mostra a saída de um formatador personalizado com uma cadeia de caracteres para os dados de propriedade.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Quando possível, use o formatador genérico para exibir seus dados, pois ele permite controlar o tamanho da DLL do analisador e fornece melhores recursos de plataforma cruzada para a DLL do analisador.

 

 

 



