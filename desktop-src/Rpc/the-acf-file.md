---
title: O arquivo ACF
description: O arquivo ACF permite que você personalize a interface RPC de seus aplicativos cliente e/ou servidor sem afetar as características de rede da interface.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917633"
---
# <a name="the-acf-file"></a>O arquivo ACF

O arquivo ACF permite que você personalize a interface RPC de seus aplicativos cliente e/ou servidor sem afetar as características de rede da interface. Por exemplo, se o aplicativo cliente contiver uma estrutura de dados complexa que tenha apenas significado no computador local, você poderá especificar no arquivo ACF como os dados nessa estrutura podem ser representados em um formato independente de computador para chamadas de procedimento remoto.

Este tutorial demonstra outro uso do arquivo ACF, especificando o tipo de identificador de associação que representa a conexão entre o cliente e o servidor. O **\[** [**atributo \_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** no cabeçalho ACF permite que o aplicativo cliente selecione um servidor para sua chamada de procedimento remoto. O ACF define o identificador para ser do identificador de [**tipo \_ t**](/windows/desktop/Midl/handle-t) (um tipo de dados primitivo MIDL). O compilador MIDL colocará o nome do identificador de associação que o ACF especificou, Hello \_ IfHandle no arquivo de cabeçalho gerado por ele. Observe que esse arquivo ACF específico tem um corpo vazio.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

O compilador MIDL tem uma opção, [**/app \_ config**](/windows/desktop/Midl/-app-config), que permite que você inclua determinados atributos de ACF, como o **\_ identificador implícito**, no arquivo IDL, em vez de criar um arquivo ACF separado. Considere usar essa opção se seu aplicativo não exigir muita configuração especial e se a compatibilidade uso estrita não for um problema.

 

 