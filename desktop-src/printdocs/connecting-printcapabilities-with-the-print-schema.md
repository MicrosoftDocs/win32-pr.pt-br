---
description: Saiba mais sobre o esquema de PrintCapabilities geral, que aborda a estrutura, a finalidade e o uso dos vários tipos de elementos.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Conectando PrintCapabilities com o esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661a8eb93c6f788381713c0c6620e8a09a53648f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409639"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Conectando PrintCapabilities com o esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema geral de PrintCapabilities aborda a estrutura, a finalidade e o uso dos vários tipos de elementos. Especifica o atributo de nome que é usado para definir instâncias específicas de cada tipo de elemento. Ele especifica que os autores de PrintCapabilities podem usar instâncias de elementos definidos pelas palavras-chave do esquema de impressão, ou podem introduzir suas próprias instâncias definidas de forma privada, desde que essas instâncias definidas de forma privada sejam definidas em um namespace claramente identificado como suas próprias. (Os autores de PrintCapabilities também podem usar instâncias definidas anteriormente em outro namespace privado.)

O documento de palavras-chave do esquema de impressão define as instâncias específicas de cada tipo de elemento disponível para uso em documentos de PrintCapabilities e em PrintTickets. Ele também documenta sua finalidade e uso. O documento de palavras-chave do esquema de impressão também define instâncias de vários tipos de elementos, da seguinte maneira:

-   Instâncias de propriedade e subpropriedade que residem na raiz do documento de PrintCapabilities

    -   Esses elementos descrevem os vários aspectos e funcionalidades do dispositivo e fornecem um vocabulário comum para descrever os dispositivos.

-   Instâncias de propriedade e subpropriedade que são filhos dos elementos de recurso

    -   Esses elementos descrevem vários aspectos relacionados a um recurso específico.

-   Instâncias de propriedade e subpropriedade que são filhos dos elementos de opção

    -   Esses elementos descrevem os vários aspectos e funcionalidades do dispositivo que dependem da opção selecionada para um recurso específico. Elas podem ser substituídas por instâncias de propriedade localizadas na raiz do documento PrintCapabilities, mas oferecem conveniência adicional em alguns casos. Para obter mais informações, consulte [adicionando instâncias de propriedade](adding-property-instances.md).

<!-- -->

-   Instâncias de ScoredProperty

    -   As instâncias ScoredProperty definem o idioma usado para caracterizar uma opção. As instâncias de ScoredProperty definidas nas palavras-chave do esquema de impressão possibilitam que as instâncias de opção escritas por muitas partes diferentes para muitos dispositivos sejam portáteis e sejam compreendidas por qualquer outro driver de dispositivo ou um provedor PrintTicket.

-   Instâncias de valor ScoredProperty

    -   Essas instâncias de valor são fornecidas pelo mesmo motivo pelo qual as instâncias de ScoredProperty são fornecidas.

-   Instâncias de recurso

    -   Cada opção deve pertencer a um recurso específico, exigindo assim que o próprio recurso seja definido.

-   Instâncias de ParameterDef

    -   Uma instância de ParameterDef de um esquema de impressão – fornecida também define um valor para cada propriedade contida nela. O provedor de PrintCapabilities é livre para modificar as instâncias de valor para as instâncias de propriedade que podem ser alteradas. Para obter informações sobre quais instâncias de propriedade podem ser alteradas e quais não podem ser alteradas (são imutáveis), consulte [ParameterDef e ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

É importante observar que o esquema de PrintCapabilities não nomea nenhuma instância de opção. As instâncias de opção são caracterizadas exclusivamente por suas instâncias ScoredProperty executadas como um todo. Um equívoco comum é que o uso do atributo ' name ' para definir uma opção identifica as instâncias de opção, mas isso está incorreto. Os elementos de opção não precisam ser exclusivos para instâncias de opção irmã, nem está usando o atributo ' name ' para definir uma opção necessária.

O documento de palavras-chave do esquema de impressão define um namespace padrão ao qual todos os atributos de nome de instância nos esquemas de PrintCapabilities e PrintTicket pertencem. Todas as marcas de tipo de elemento e atributos XML usados pelos tipos de elemento também pertencem a esse namespace.

Para cada instância definida no esquema PrintCapabilities, o esquema PrintCapabilities especifica o atributo Name e o local da instância. O provedor e o cliente devem preservar ambos ao usar essa instância no documento ou PrintTicket de PrintCapabilities.

O documento de palavras-chave do esquema de impressão designa algumas instâncias como obrigatórias. Essas instâncias devem aparecer em cada documento de PrintCapabilities e devem ser inicializadas corretamente com valores válidos. Todas as instâncias nas palavras-chave do esquema de impressão que não são designadas como obrigatórias são opcionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



