---
description: Descreve o arquivo de configuração WsdCodeGen.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: Arquivo de configuração WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091272"
---
# <a name="wsdcodegen-configuration-file"></a>Arquivo de configuração WsdCodeGen

Um arquivo de configuração WsdCodeGen geralmente é gerado pela ferramenta WsdCodeGen. Você pode criar arquivos de configuração manualmente, mas a complexidade e o comprimento do arquivo normalmente impedim a codificação manual. É altamente recomendável usar WsdCodeGen para gerar o arquivo. Para obter mais informações sobre como gerar arquivos de configuração, consulte usando a [sintaxe de linha de comando](wsdcodegen-command-line-syntax.md) [WsdCodeGen](using-wsdcodegen.md) e WsdCodeGen.

Você deve inspecionar o arquivo de configuração gerado e, se necessário, modificá-lo antes de usá-lo para criar o código-fonte. O arquivo de configuração gerado pelo WsdCodeGen normalmente é suficiente para a maioria dos desenvolvimentos de cliente.

Para usar o arquivo de configuração para o desenvolvimento de servidor, algumas modificações são necessárias. Se a hospedagem estiver habilitada (ou seja, se o modo "todos" ou "host" estiver selecionado), modifique o conteúdo do elemento [**ThisModelMetadata**](thismodelmetadata.md) e seus elementos filho, conforme necessário. Além disso, modifique ou remova os elementos [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid) dentro do elemento **ThisModelMetadata** ou dos elementos [**hospedados**](hosted.md) , conforme necessário.

Um arquivo de configuração consiste em uma sequência de elementos que fornece dados de entrada para geração de código seguida por qualquer número de elementos de [**arquivo**](file.md) que descrevem os arquivos a serem gerados. Os dados de entrada incluem algumas propriedades globais e referências a tipos expressos em WSDL, XSD e assemblies gerenciados. Texto e CDATA em elementos de **arquivo** são gravados nos arquivos gerados sem modificação. Outros elementos em elementos de **arquivo** são substituídos nos arquivos gerados com o código gerado.

Os arquivos de configuração XML devem seguir algumas regras gerais para que sejam formatados corretamente para uso com o utilitário gerador de código. Eles são:

-   O elemento raiz de qualquer arquivo de configuração é [**wsdCodeGen**](wsdcodegen.md).

-   Elementos que contêm tipos de dados simples são intercambiáveis com atributos. Por exemplo:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    é equivalente a:

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   Em geral, não há nenhuma restrição na ordenação de elementos. Por exemplo:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    é equivalente a:

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    No entanto, o gerador de código processa o arquivo de configuração em uma única passagem, e a ordenação tem alguma relevância. Por exemplo, os elementos de [**arquivo**](file.md) que geram código relacionado a um tipo de porta específico devem ocorrer após o elemento que instrui o gerador de código a ler o contrato de tipo de porta.

Para obter uma lista completa dos elementos usados nos arquivos de configuração do WsdCodeGen, consulte [referência XML do arquivo de configuração do WsdCodeGen](wsdcodegen-configuration-file-xml-reference.md).

Os arquivos de configuração de exemplo estão incluídos no SDK do Windows. Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Exemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 
