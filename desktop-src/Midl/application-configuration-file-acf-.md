---
title: Arquivo de configuração de aplicativo (ACF)
description: Pode haver aspectos do seu aplicativo distribuído que afetam um componente, mas não têm nada a ver com outro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Linguagem IDL da Microsoft MIDL, descrito, arquivo de configuração de aplicativo
- arquivo de configuração de aplicativo MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748604"
---
# <a name="application-configuration-file-acf"></a>Arquivo de configuração de aplicativo (ACF)

Pode haver aspectos do seu aplicativo distribuído que afetam um componente, mas não têm nada a ver com outro. Por exemplo, um objeto pode conter uma estrutura de dados grande e complexa e passar o conteúdo dessa estrutura de dados para outro objeto. O layout exato dessa estrutura de dados pode não ser sentido para o aplicativo de recebimento. Além disso, a estrutura pode conter tipos de dados que o compilador MIDL não reconhece e não pode gerar empacotamento e desempacotamento de código.

Os aplicativos cliente podem compartilhar a mesma interface, mas são executados em diferentes plataformas; Eles podem precisar de seu próprio conjunto de rotinas de marshaling. Por fim, os clientes individuais talvez nem sempre precisem do mesmo conjunto de funções. Não é eficiente gerar código stub para funções que nunca serão implementadas em um determinado aplicativo cliente.

Ao definir esses aspectos locais de sua interface em um arquivo de configuração de aplicativo (ACF), você pode separar as diferenças entre as interfaces de cliente de sua representação de rede, permitindo que o servidor envie e receba dados em um formato consistente e tornando seu código stub mais compacto e eficiente.

A estrutura e a sintaxe de uma definição de interface ACF são idênticas à definição de IDL:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Por padrão, o nome da interface ACF deve corresponder ao seu nome na definição de IDL. No entanto, quando você usa a opção de compilador MIDL/ [**ACF**](-acf.md) para especificar explicitamente um nome de arquivo ACF, os nomes de interface não precisam corresponder. Esse recurso permite que várias interfaces compartilhem uma única especificação de ACF.

 

 




