---
description: O exemplo de código PropertyEdit demonstra como converter o nome da propriedade canônica em um PROPERTYKEY, definir o valor do repositório de propriedades para o do item e gravar os dados de volta no fluxo de arquivos.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826913"
---
# <a name="propertyedit"></a>PropertyEdit

O exemplo de código PropertyEdit demonstra como converter o nome da propriedade canônica em um PROPERTYKEY, definir o valor do repositório de propriedades para o do item e gravar os dados de volta no fluxo de arquivos.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Produto     | Versão mínima do produto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| SDK do Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local      | URL do caminho                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Exemplo de PropertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **PropertyEdit** . 
2.  Digite `msbuild PropertyEdit.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **PropertyEdit** .
2.  Clique duas vezes no ícone do arquivo PropertyEdit. sln para abrir o projeto no Visual Studio.
    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2.  No prompt de comando, digite `PropertyEdit.exe` ou, no Windows Explorer, clique duas vezes no ícone para PropertyEdit.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Exemplos de código de pesquisa](-search-samples-ovw.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Sobre manipuladores de propriedade e propriedades](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Esquema de descrição da propriedade](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
