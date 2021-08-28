---
description: Veja como o autor de um cliente PrintTicket pode usar tipos de elemento para criar um PrintTicket que descreve as intenções de um dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de verificação de construção printTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6a3ae0c19fea01738dbf7c6ecfa52f6f156d59f67dae89d6d5a2952059a765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091716"
---
# <a name="printticket-construction-checklists"></a>Listas de verificação de construção printTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esta seção demonstra como o autor de um cliente PrintTicket pode usar os tipos de elemento definidos no Print Schema Framework para criar um PrintTicket que descreve as intenções de um dispositivo. O PrintTicket pode ser genérico (não vinculado a um dispositivo específico) ou pode ser específico do dispositivo. A semântica do PrintTicket é apresentada em mais detalhes. Além disso, esta seção contém uma visão geral dos conceitos e da terminologia que são abordados mais detalhadamente nas seções subsequentes.

Há duas abordagens fundamentalmente diferentes para construir um PrintTicket. Qualquer abordagem pode ser usada.

-   Direcionar o PrintTicket para um dispositivo desconhecido ou genérico criando [um PrintTicket genérico.](creating-a-generic-printticket.md)

    Se seu objetivo principal for preservar a intenção do usuário final, talvez você queira tomar essa abordagem, construindo e armazenar um PrintTicket genérico nãovalidado com o documento.

-   Direcionar o PrintTicket para um dispositivo específico, criando [um Device-Specific PrintTicket.](creating-a-device-specific-printticket.md)

    Se estiver mais interessado em aproveitar todos os recursos oferecidos por um dispositivo específico, talvez você queira tomar essa abordagem, construindo um PrintTicket para o dispositivo específico e armazenar o PrintTicket validado com o documento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



