---
description: Leia sobre os recursos e as opções em um documento de PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Recursos e opções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6d0918b6237885c2c7240efb0dc0f982b882f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549404"
---
# <a name="features-and-options"></a>Recursos e opções

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As construções de recurso/opção e de parâmetro são usadas em um documento de PrintCapabilities para representar atributos de dispositivo que contribuem para a definição da configuração do dispositivo. Para obter um exemplo de um constructo de recurso/opção, considere um dispositivo de impressão capaz de imprimir em várias resoluções. O atributo de dispositivo que define a resolução pode ser representado como uma instância de recurso, com cada um dos valores de resolução de saída possíveis representados como uma instância de opção individual. Uma instância de opção pode representar uma resolução de 300 dpi, outra pode representar uma resolução de 600 dpi e assim por diante.

Deve-se observar que o esquema de impressão requer que a lista de instâncias de recurso, opção e ParameterDef relatadas em cada documento de PrintCapabilities deve permanecer constante, independentemente da configuração. Isso permite que as configurações e dependências das configurações sejam expressas de forma não ambígua. A implicação desse requisito é que cada recurso e subrecurso devem ter uma configuração bem definida, independentemente da configuração de qualquer outro recurso ou subrecurso. Portanto, cada subrecurso deve ter uma opção equivalente a uma configuração não operacional (uma definição desativada, desabilitada ou nenhuma), que é selecionada automaticamente para todos os sub-recursos quando o usuário seleciona a opção não op no recurso pai. Por outro lado, quando um dos sub-recursos é definido como uma opção habilitada, o recurso pai e outros sub-recursos associados também são habilitados. Enquanto isso, o provedor PrintTicket deve garantir (durante a validação de PrintTicket) que as configurações de todas as instâncias de recurso e de subrecurso são definidas, independentemente da configuração do dispositivo, e que as configurações do subrecurso são consistentes com as configurações do recurso pai. Isso garante que o dispositivo não recebe um PrintTicket inconsistente em que alguns sub-recursos indicam que, por exemplo, o grampeamento está habilitado, mas outros sub-recursos indicam que o grampeamento está desabilitado.

Observe que os autores de PrintCapabilities não precisam utilizar os recursos de aninhamento dos elementos de recurso. Se preferir, eles podem apresentar todas as instâncias de recurso em uma estrutura plana, como irmãos entre si. Observe também que uma coleção aninhada de instâncias de recursos pode ser achatada simplesmente movendo todos os sub-recursos para o nível raiz. A única precaução que deve ser tomada é garantir que os atributos de nome dessas instâncias de recursos sejam exclusivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



