---
description: Monitor de Rede ou a DLL do analisador podem formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formatar os dados exibidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501353"
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

 

 

 



