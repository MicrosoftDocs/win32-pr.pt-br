---
description: O Esquema de Impressão aborda a opacidade e ambiguidade na comunicação entre componentes do subsistema de impressão e entre o subsistema de impressão e os aplicativos.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Tela de fundo do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab366429623f2bb1f187294705d1a83e93acd1e5fb500d4b1e9d224496ac39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731756"
---
# <a name="print-schema-background"></a>Tela de fundo do esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O Esquema de Impressão destina-se a resolver os problemas de opacidade e ambiguidade associados à comunicação interna entre os componentes do subsistema de impressão e comunicação externa entre o subsistema de impressão e os aplicativos.

A interação atual do subsistema de impressão com os plug-ins de aplicativos e fornecedores de hardware usa a estrutura DEVMODE binária baseada em índice e o DevCaps binário. Configurações feitas por cada componente são amplamente opacas para outros componentes, impedindo a portabilidade de configurações entre dispositivos ou até mesmo entre diferentes versões de driver no mesmo dispositivo. Além disso, PrintCapabilities não pode ser facilmente aproveitado por aplicativos cliente sem conhecimento proprietário do dispositivo ou usando a interface do usuário do driver. Além dessas limitações, em um sentido mais amplo, não há uma linguagem bem definida para descrever atributos gerais do dispositivo, PrintCapabilities, configurações de dispositivo ou formatação de trabalho. O Esquema de Impressão e suas tecnologias relacionadas foram projetados para resolver essas limitações, fornecendo um método consistente, não ambíguo e extensível de comunicação de configurações e funcionalidades de maneira consolidada e lógica.

As bases conceituais das Palavras-chave de Esquema de Impressão e da Estrutura de Esquema de Impressão são consistência, falta de ambiguidade e extensibilidade. A consistência é alcançada por meio do uso das Palavras-chave de esquema de impressão e da Estrutura de Esquema de Impressão como os blocos de construção para a comunicação entre componentes de impressão de última geração. Os aplicativos, o subsistema de impressão Windows Microsoft e os plug-ins e drivers IHV interagem usando esse mecanismo comum. Essas palavras-chave, sua estrutura e seu significado serão bem definidos pelo esquema público. Isso impede a ambiguidade no significado de uma palavra-chave específica e impede palavras-chave redundantes ou duplicadas. Todos os componentes podem contar com o uso de uma palavra-chave específica para transmitir uma determinada intenção e fazer com que essa intenção seja bem compreendida pelo destinatário. A extensibilidade é essencial para ser a longevidade das Palavras-chave de esquema de impressão, garantindo que o esquema público seja uma entidade dinâmica. A estrutura também permite extensões privadas, que concede aos IHVs a flexibilidade de inovar conforme desejado, ter em mente a inclusão futura de uma palavra-chave privada no esquema público é essencial para preservar a consistência e evitar a ambiguidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



