---
title: Esquemas e documentos de PrintCapabilities
description: O esquema de PrintCapabilities é destinado a eliminar muitas das limitações das funções DevCaps do Win32.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21347fae1c9824df4a8355f8dd26de37eeac4604
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407069"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Construção de esquema e documento de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As funções atuais do Win32 DevCaps (como GetDeviceCaps ou DeviceCapabilities, ambas descritas na documentação do kit de desenvolvimento de software da plataforma Microsoft (SDK)) limitam severamente o tipo de informação que os componentes que não são de driver podem obter, com relação aos recursos e propriedades dos dispositivos de impressão. Não há suporte para a publicação dos recursos de processadores de impressão, nem há um método para enumerar recursos não padrão. Portanto, não há como um componente que não seja um driver para construir uma interface de usuário completa. Além disso, o cliente ou aplicativo não pode determinar completamente os recursos de dispositivos ou filas de impressão além daqueles fornecidos pelas funções DevCaps do Win32. As funções atuais não são extensíveis, de modo que os dispositivos não podem publicar novas propriedades ou recursos.

O esquema PrintCapabilities destina-se a eliminar muitas das limitações das funções DevCaps do Win32, fornecendo um superconjunto da funcionalidade acessível por essas funções. Se mais funcionalidades forem necessárias, um provedor do documento PrintCapabilities poderá estender as palavras-chave do esquema de impressão, dentro das restrições da estrutura de esquema de impressão, adicionando instâncias de elementos definidas de modo privado. Devido à sua dependência em XML como a mídia de intercâmbio, qualquer consumidor de um documento de PrintCapabilities pode acessar todos os dados no documento sem restrição e sem preocupação com a compatibilidade com versões diferentes do sistema operacional. Esta seção descreve o esquema de PrintCapabilities e detalha seu uso.

O público-alvo desta seção inclui os seguintes grupos:

-   Implementadores da interface do provedor PrintTicket/PrintCapabilities

-   Consumidores de PrintCapabilities

-   Clientes da interface do provedor PrintTicket/PrintCapabilities

A primeira categoria na lista anterior é conhecida como provedores de PrintCapabilities no restante desta seção. A segunda e a terceira categorias são chamadas de consumidores de PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relação para imprimir esquema e esquema PrintTicket

Os esquemas de PrintCapabilities e PrintTicket são partes especializadas do esquema de impressão. As principais diferenças estruturais entre esses subconjuntos do esquema de impressão são que o esquema de PrintCapabilities inclui as instâncias de propriedade e ParameterDef que não estão contidas no esquema PrintTicket, enquanto o esquema PrintTicket contém as instâncias de propriedade e ParameterInit que não estão contidas no esquema de PrintCapabilities. Exceto por essas diferenças, os esquemas de PrintCapabilities e PrintTicket geralmente são espelhados em conteúdo, compartilhando recursos, opções, ScoredProperty e instâncias de valor. Qualquer conteúdo compartilhado deve ser mantido atualizado. Por exemplo, se uma alteração for feita no recurso PageMediaSize no esquema PrintCapabilities, a mesma alteração deverá ser feita no esquema PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



