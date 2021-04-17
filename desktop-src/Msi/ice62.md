---
description: O ICE62 executa verificações extensivas na tabela IsolatedComponent para dados que podem causar um comportamento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768468"
---
# <a name="ice62"></a>ICE62

O ICE62 executa verificações extensivas na [tabela IsolatedComponent](isolatedcomponent-table.md) para dados que podem causar um comportamento inesperado.

A falha na correção de um erro relatado pelo ICE62 pode resultar em uma falha do sistema de componentes isolado em uma ampla variedade de formas. Por exemplo, se o bit SharedDllRefCount não estiver definido para um componente compartilhado, o registro do componente poderá ser removido quando outro aplicativo usar esse ComponentID e for desinstalado.

## <a name="result"></a>Resultado

ICE62 posta um aviso ou erro quando encontra dados na tabela IsolatedComponent que podem produzir um comportamento inesperado.

## <a name="example"></a>Exemplo

ICE62 relata os erros e avisos a seguir para os exemplos mostrados.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 é listado como o componente de aplicativo para o isolamento de Component1. No entanto, Component2 tem um caminho de chave do registro e não fornece um caminho executável válido a ser usado para isolar o componente.

Para corrigir esse erro, use um componente diferente como o aplicativo para o componente isolado Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 está listado como um componente compartilhado isolado, mas não tem o conjunto de bits SharedDllRefCount. Isso pode resultar no tempo de vida do componente estar incorreto. Se outro aplicativo usar esse componente (isolado ou não) e for desinstalado, o registro do componente será removido, mas a cópia isolada desse aplicativo permanecerá. Isso causa problemas de reparo e desinstalação.

Para corrigir esse erro, defina o bit SharedDllRefCount para o componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 e Component2 são instalados por diferentes recursos. O Component1 é instalado pelo Feature1 e o Component2 é instalado pelo Feature2. Feature1 não é pai de Feature2, portanto, é possível que o aplicativo seja instalado, mas não o componente isolado, dividindo o isolamento.

Para corrigir esse erro, adicione uma entrada à tabela FeatureComponents vinculando Component1 ao mesmo recurso que (ou um recurso pai do) o recurso que instala o Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 tem uma condição na tabela de componentes. Se essa condição mudar de TRUE para FALSE durante o tempo de vida de uma instalação em um computador, o componente isolado poderá ficar órfão sem informações de registro.

Para corrigir esse aviso, remova a condição ou crie a condição para que ela nunca possa ser alterada de verdadeira para falsa.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 é isolado para Component2 e Component3, e os dois componentes também são instalados no mesmo diretório. Os aplicativos compartilham um componente isolado, mas se um aplicativo for removido, o componente compartilhado também será removido, fazendo com que os outros aplicativos percam o componente isolado.

Para corrigir esse aviso, instale os aplicativos em diretórios diferentes ou verifique se alguns dos aplicativos realmente exigem um componente isolado.

[Tabela IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartilhado | Aplicativo de componente \_ |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Tabela de componentes](component-table.md)



| Componente  | ComponentId | Diretório\_ | Atributos | Condição   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MyCondition | Arquivo1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | Arquivo3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  | Pai do recurso \_ |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



