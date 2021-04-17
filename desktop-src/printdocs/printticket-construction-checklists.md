---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de verificação de construção do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763244"
---
# <a name="printticket-construction-checklists"></a>Listas de verificação de construção do PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esta seção demonstra como o autor de um cliente PrintTicket pode usar os tipos de elemento definidos na estrutura de esquema de impressão para criar um PrintTicket que descreve as intenções de um dispositivo. O PrintTicket pode ser genérico (não vinculado a um dispositivo específico) ou pode ser específico do dispositivo. A semântica do PrintTicket é apresentada mais detalhadamente. Além disso, esta seção contém uma visão geral dos conceitos e da terminologia que são abordados em mais detalhes nas seções subsequentes.

Há duas abordagens fundamentalmente diferentes para construir um PrintTicket. Qualquer uma das abordagens pode ser usada.

-   Direcione o PrintTicket para um dispositivo desconhecido ou genérico [criando um PrintTicket genérico](creating-a-generic-printticket.md).

    Se seu objetivo principal é preservar a intenção do usuário final, talvez você queira adotar essa abordagem, construindo e armazenando um PrintTicket genérico não validado com o documento.

-   Direcione o PrintTicket para um dispositivo específico, [criando um Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Se você estiver mais interessado em aproveitar todos os recursos oferecidos por um determinado dispositivo, talvez queira adotar essa abordagem criando um PrintTicket para o dispositivo específico e armazenando o PrintTicket validado com o documento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



