---
title: O arquivo ACF
description: O arquivo ACF permite personalizar a interface RPC dos aplicativos cliente e/ou servidor sem afetar as características de rede da interface.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d234b30c25870dd7a21cb790cc4839236ab69093291285b64c870cf7c05cb11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080836"
---
# <a name="the-acf-file"></a>O arquivo ACF

O arquivo ACF permite personalizar a interface RPC dos aplicativos cliente e/ou servidor sem afetar as características de rede da interface. Por exemplo, se o aplicativo cliente contiver uma estrutura de dados complexa que tenha significado apenas no computador local, você poderá especificar no arquivo ACF como os dados nessa estrutura podem ser representados em um formulário independente de computador para chamadas de procedimento remoto.

Este tutorial demonstra outro uso do arquivo ACF – especificando o tipo de identificador de associação que representa a conexão entre o cliente e o servidor. O **\[** [**atributo de \_ alça**](/windows/desktop/Midl/implicit-handle) implícita no header do ACF permite que o aplicativo cliente selecione **\]** um servidor para sua chamada de procedimento remoto. O ACF define o identificador para ser do tipo [**identificador \_ t**](/windows/desktop/Midl/handle-t) (um tipo de dados primitivo MIDL). O compilador MIDL colocará o nome do alça de associação especificado pelo ACF, hello IfHandle no arquivo \_ de header que ele gera. Observe que esse arquivo ACF específico tem um corpo vazio.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

O compilador MIDL tem uma opção, [**/app \_ config**](/windows/desktop/Midl/-app-config), que permite incluir determinados atributos do ACF, como o handle implícito **, \_** no arquivo IDL, em vez de criar um arquivo ACF separado. Considere usar essa opção se seu aplicativo não exigir muita configuração especial e se a compatibilidade de OSF estrita não for um problema.

 

 