---
description: Saiba mais sobre o formato PrintTicket, que expressa informações de configuração usando a Estrutura de Esquema de Impressão baseada em XML.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Esquema PrintTicket e construção de documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5998aeb534bbbeb16681a4136cf33425a7eefad7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405429"
---
# <a name="printticket-schema-and-document-construction"></a>Esquema PrintTicket e construção de documento

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O método atual de especificar informações de configuração de dispositivo usando uma estrutura DEVMODE sofre de várias limitações. Primeiro, a estrutura DEVMODE é uma estrutura binária, que pode levar a problemas de versões diferentes. Em segundo lugar, ele é dividido em uma parte pública inexistível e uma parte privada que pode ser acessada somente por drivers e somente então pelo driver específico que a criou. O formato PrintTicket expressa informações de configuração usando a Estrutura de Esquema de Impressão baseada em XML, eliminando assim essas deficiências da estrutura DEVMODE.

O esquema PrintTicket aborda cada um dos dois problemas mencionados. Primeiro, o Esquema PrintTicket é um arquivo de texto baseado em XML, portanto, os problemas de extensibilidade e de versão são eliminados. Em segundo lugar, as informações de configuração estão disponíveis para todos os clientes, o que significa que qualquer cliente ou provedor pode armazenar e recuperar todas as informações contidas em um PrintTicket. As opções são descritas usando a mesma técnica usada pela Estrutura de Esquema de Impressão e pelo documento PrintCapabilities derivado. Por esse motivo, o PrintTicket fornece todos os possíveis benefícios de portabilidade do modelo de definição de opção a ser realizado. Consulte [Print Schema Framework para](print-schema-framework.md) obter mais informações. O público-alvo desta seção inclui os seguintes grupos:

-   Implementadores de uma interface do provedor PrintTicket/PrintCapabilities

-   Consumidores do PrintTicket

-   Clientes de uma interface do provedor PrintTicket/PrintCapabilities

Os membros da primeira categoria na lista anterior são chamados de provedores PrintTicket no restante desta seção. Os membros das duas últimas categorias são chamados de consumidores PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relação com o esquema de impressão e o esquema PrintCapabilities

Os esquemas PrintTicket e PrintCapabilities são partes especializadas do esquema de impressão. As principais diferenças estruturais entre esses subconjunto do esquema de impressão são que o esquema PrintTicket contém instâncias Property e ParameterInit que não estão contidas no esquema PrintCapabilities, enquanto o esquema PrintCapabilities inclui instâncias Property e ParameterDef que não estão contidas no esquema PrintTicket. Exceto por essas diferenças, os esquemas PrintCapabilities e PrintTicket geralmente espelham uns aos outros nas instâncias de conteúdo, compartilhamento de Recurso, Opção, ScoredProperty e Valor. Qualquer conteúdo compartilhado desse tipo deve ser mantido atualizado. Por exemplo, se uma alteração for feita no Recurso MediaSize no Esquema PrintCapabilities, a mesma alteração deverá ser feita no esquema PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



