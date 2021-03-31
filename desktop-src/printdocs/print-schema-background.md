---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Plano de fundo do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103663844"
---
# <a name="print-schema-background"></a>Plano de fundo do esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema de impressão destina-se a resolver os problemas de opaco e ambiguidade associados à comunicação interna entre os componentes do subsistema de impressão e a comunicação externa entre o subsistema de impressão e os aplicativos.

A interação do subsistema de impressão atual com os plug-ins de aplicativos e fornecedores de hardware usa a estrutura DEVMODE binária, baseada em índice e a DevCaps binária. As configurações feitas por cada componente são amplamente opacas para outros componentes, impedindo a portabilidade das configurações entre dispositivos ou mesmo entre versões de driver diferentes no mesmo dispositivo. Além disso, os PrintCapabilities não podem ser facilmente aproveitados por aplicativos cliente sem o conhecimento proprietário do dispositivo ou usando a interface do usuário do driver. Além dessas limitações, em um sentido mais amplo, não há linguagem bem definida para descrever os atributos gerais do dispositivo, as PrintCapabilities, as configurações do dispositivo ou a formatação do trabalho. O esquema de impressão e suas tecnologias relacionadas são projetados para resolver essas limitações, fornecendo um método consistente, inequívoca e extensível de comunicação de configurações e recursos de maneira consolidada e lógica.

As bases conceituais das palavras-chave do esquema de impressão e da estrutura de esquema de impressão são consistência, falta de ambiguidade e extensibilidade. A consistência é obtida por meio do uso das palavras-chave do esquema de impressão e da estrutura de esquema de impressão como os blocos de construção para a comunicação entre os componentes de impressão da próxima geração. Os aplicativos, o subsistema de impressão do Microsoft Windows e os plug-ins e os drivers de IHV interagem usando esse mecanismo comum. Essas palavras-chave, sua estrutura e seu significado, serão bem definidas pelo esquema público. Isso evita ambigüidade no significado de uma palavra-chave específica e impede palavras-chave redundantes ou duplicadas. Todos os componentes podem contar com o uso de uma palavra-chave específica para transmitir uma determinada intenção e fazer com que essa intenção seja bem compreendida pelo destinatário. A extensibilidade é vital para ser a longevidade das palavras-chave do esquema de impressão, garantindo que o esquema público seja uma entidade dinâmica. A estrutura também permite extensões privadas, o que concede aos IHVs a flexibilidade de inovar conforme desejado, tendo em mente a inclusão futura de uma palavra-chave privada no esquema público é essencial para preservar a consistência e impedir a ambiguidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



