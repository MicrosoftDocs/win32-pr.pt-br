---
description: O ICE62 executa verificações extensivas na tabela IsolatedComponent para dados que podem causar um comportamento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528236"
---
# <a name="ice62"></a>ICE62

O ICE62 executa verificações extensivas na [tabela IsolatedComponent](isolatedcomponent-table.md) para dados que podem causar um comportamento inesperado.

A falha ao corrigir um erro relatado pelo ICE62 pode resultar em uma falha do sistema de componente isolado de várias maneiras. Por exemplo, se o bit SharedDllRefCount não estiver definido para um componente compartilhado, o registro do componente poderá ser removido quando outro aplicativo usar essa ComponentId e for desinstalado.

## <a name="result"></a>Resultado

O ICE62 posta um aviso ou erro quando encontra dados na tabela IsolatedComponent que podem produzir um comportamento inesperado.

## <a name="example"></a>Exemplo

O ICE62 relata os seguintes erros e avisos para os exemplos mostrados.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 é listado como o componente do aplicativo para o isolamento do component1. No entanto, Component2 tem um caminho de chave do Registro e não fornece um caminho executável válido a ser usado para isolar o componente.

Para corrigir esse erro, use um componente diferente como o aplicativo para o componente isolado Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 é listado como um componente compartilhado isolado, mas não tem o bit SharedDllRefCount definido. Isso pode fazer com que o tempo de vida do componente seja incorreto. Se outro aplicativo usar esse componente (isolado ou não) e for desinstalado, o registro do componente será removido, mas a cópia isolada do aplicativo permanecerá. Isso causa problemas de reparo e desinstalação.

Para corrigir esse erro, de definido o bit SharedDllRefCount para o componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 e Component2 são instalados por recursos diferentes. Component1 é instalado pelo Feature1 e Component2 é instalado pelo Feature2. Feature1 não é um pai do Feature2, portanto, é possível que o aplicativo seja instalado, mas não o componente isolado, quebrando o isolamento.

Para corrigir esse erro, adicione uma entrada à tabela FeatureComponents vinculando Component1 ao mesmo recurso que (ou um recurso pai do) o recurso que instala o Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 tem uma condição na tabela Componente. Se essa condição mudar de TRUE para FALSE durante o tempo de vida de uma instalação em um computador, o componente isolado poderá ficar órfão sem informações de registro.

Para corrigir esse aviso, remova a condição ou autor da condição para que ela nunca possa mudar de TRUE para FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 é isolado para Component2 e Component3, e os dois componentes também são instalados no mesmo diretório. Os aplicativos compartilham um componente isolado, mas se um aplicativo for removido, o componente compartilhado será removido, fazendo com que os outros aplicativos percam o componente isolado.

Para corrigir esse aviso, instale os aplicativos em diretórios diferentes ou verifique se alguns dos aplicativos realmente exigem um componente isolado.

[Tabela IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ Compartilhado | Aplicativo \_ de componente |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Tabela de componentes](component-table.md)



| Componente  | Componentid | Diretório\_ | Atributos | Condição   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MYCONDITION | Arquivo1     |
| Component2 |             | Targetdir   | 4          |             | Registro2 |
| Component3 |             | Targetdir   | 0          |             | Arquivo3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  | Pai do \_ recurso |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



