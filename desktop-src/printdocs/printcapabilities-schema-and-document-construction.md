---
title: Esquemas e documentos printCapabilities
description: O esquema PrintCapabilities destina-se a eliminar muitas das limitações das funções Win32 DevCaps.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd79c81beceecea4a660fd2376a759e470670a414a7cad4a8ac26be086688e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711616"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Esquema PrintCapabilities e construção de documentos

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As funções atuais do Win32 DevCaps (como GetDeviceCaps ou DeviceCapabilities, ambas descritas na documentação do Microsoft Platform Software Development Kit (SDK) limitam gravemente o tipo de informações que os componentes que não são do driver podem obter, em relação aos recursos e propriedades dos dispositivos de impressão. Não há suporte para publicar os recursos de processadores de impressão, nem há um método para enumerar recursos não padrão. Portanto, não há como um componente diferente de um driver construir uma interface do usuário completa. Além disso, o cliente ou aplicativo não pode determinar completamente os recursos de dispositivos ou filas de impressão além daqueles fornecidos pelas funções win32 DevCaps. As funções atuais não são extensíveis, portanto, os dispositivos não podem publicar novas propriedades ou recursos.

O esquema PrintCapabilities destina-se a eliminar muitas das limitações das funções win32 DevCaps fornecendo um superconjunto da funcionalidade proporcionada por essas funções. Se mais funcionalidade for necessária, um provedor do documento PrintCapabilities poderá estender as Palavras-chave de esquema de impressão, dentro das restrições da Estrutura de Esquema de Impressão, adicionando instâncias de elemento definidas de forma privada. Devido à sua dependência no XML como o meio de intercâmbio, qualquer consumidor de um documento PrintCapabilities pode acessar todos os dados no documento sem restrição e sem se preocupar com a compatibilidade com diferentes versões do sistema operacional. Esta seção descreve o esquema PrintCapabilities e detalha seu uso.

O público-alvo desta seção inclui os seguintes grupos:

-   Implementadores da interface do provedor PrintTicket/PrintCapabilities

-   Consumidores de PrintCapabilities

-   Clientes da interface do provedor PrintTicket/PrintCapabilities

A primeira categoria na lista anterior é conhecida como provedores PrintCapabilities no restante desta seção. A segunda e a terceira categorias são conhecidas como consumidores PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relação com o esquema de impressão e o esquema PrintTicket

Os esquemas PrintCapabilities e PrintTicket são partes especializadas do esquema de impressão. As principais diferenças estruturais entre esses subconjunto do esquema de impressão são que o esquema PrintCapabilities inclui instâncias Property e ParameterDef que não estão contidas no esquema PrintTicket, enquanto o esquema PrintTicket contém instâncias Property e ParameterInit que não estão contidas no esquema PrintCapabilities. Exceto por essas diferenças, os esquemas PrintCapabilities e PrintTicket geralmente espelham uns aos outros em conteúdo, compartilhando Recurso, Opção, ScoredProperty e Instâncias de Valor. Qualquer conteúdo compartilhado desse tipo deve ser mantido atualizado. Por exemplo, se uma alteração for feita no recurso PageMediaSize no esquema PrintCapabilities, a mesma alteração deverá ser feita no esquema PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



