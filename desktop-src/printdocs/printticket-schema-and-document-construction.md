---
description: Saiba mais sobre o formato PrintTicket, que expressa informações de configuração usando a estrutura de esquema de impressão baseada em XML.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Construção de esquema e documento do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6de44ad04e9e39a516af0842bfaaca5b081191cb322b2f3a96f919590c64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824436"
---
# <a name="printticket-schema-and-document-construction"></a>Construção de esquema e documento do PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O método atual de especificar as informações de configuração do dispositivo usando uma estrutura DEVMODE sofre de várias limitações. Primeiro, a estrutura DEVMODE é uma estrutura binária, o que pode levar a problemas de diferentes versões. Em segundo lugar, ele é dividido em uma parte pública não extensível e uma parte privada que pode ser acessada somente por drivers e, em seguida, pelo driver específico que o criou. O formato PrintTicket expressa informações de configuração usando a estrutura de esquema de impressão baseada em XML, eliminando assim essas deficiências da estrutura DEVMODE.

O esquema PrintTicket aborda cada um dos dois problemas que acabamos de mencionar. Primeiro, o esquema PrintTicket é um arquivo de texto baseado em XML, de modo que os problemas com extensibilidade e controle de versão sejam eliminados. Segundo, as informações de configuração estão disponíveis para todos os clientes, o que significa que qualquer cliente ou provedor pode armazenar e recuperar qualquer informação contida em um PrintTicket. As opções são descritas usando a mesma técnica usada pela estrutura de esquema de impressão e o documento de PrintCapabilities derivado. Por esse motivo, o PrintTicket fornece todos os benefícios de portabilidade em potencial do modelo de definição de opção a ser realizado. Consulte [Imprimir estrutura do esquema](print-schema-framework.md) para obter mais informações. O público-alvo desta seção inclui os seguintes grupos:

-   Implementadores de uma interface de provedor PrintTicket/PrintCapabilities

-   Consumidores do PrintTicket

-   Clientes de uma interface de provedor PrintTicket/PrintCapabilities

Os membros da primeira categoria na lista anterior são chamados de provedores de PrintTicket no restante desta seção. Os membros das duas últimas categorias são chamados de consumidores de PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relação para imprimir esquema e esquema de PrintCapabilities

Os esquemas PrintTicket e PrintCapabilities são partes especializadas do esquema de impressão. As principais diferenças estruturais entre esses subconjuntos do esquema de impressão são que o esquema PrintTicket contém instâncias de propriedade e ParameterInit que não estão contidas no esquema de PrintCapabilities, enquanto o esquema de PrintCapabilities inclui as instâncias de propriedade e ParameterDef que não estão contidas no esquema PrintTicket. Exceto por essas diferenças, os esquemas de PrintCapabilities e PrintTicket geralmente são espelhados em conteúdo, compartilhando recursos, opções, ScoredProperty e instâncias de valor. Qualquer conteúdo compartilhado deve ser mantido atualizado. Por exemplo, se uma alteração for feita no recurso MediaSize no esquema PrintCapabilities, a mesma alteração deverá ser feita no esquema PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



