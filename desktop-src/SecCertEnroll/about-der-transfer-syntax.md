---
description: A aplicação de uma regra de codificação às estruturas de dados descritas por uma sintaxe abstrata fornece uma sintaxe de transferência que governa como os bytes em um fluxo são organizados quando enviados entre computadores.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintaxe de transferência de DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6757a22743a2c44abb5ef4c46154a08e425e2b1b7045beaacc7fb4f4f206fed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904505"
---
# <a name="der-transfer-syntax"></a>Sintaxe de transferência de DER

A aplicação de uma regra de codificação às estruturas de dados descritas por uma sintaxe abstrata fornece uma sintaxe de transferência que governa como os bytes em um fluxo são organizados quando enviados entre computadores. a sintaxe de transferência usada pelo Distinguished Encoding Rules sempre segue um formato *de marca, comprimento e valor* . O formato geralmente é conhecido como um TLV terceto em que cada campo (T, L ou V) contém um ou mais bytes.

![tipo de der, comprimento e valor (TLV) terceto](images/der-tlv-basic.png)

O campo de *marca* especifica o tipo da estrutura de dados que está sendo enviada, o campo *comprimento* especifica o número de bytes de conteúdo que está sendo transferido e o campo *valor* contém o conteúdo. Observe que o campo de *valor* pode ser um terceto se ele contiver um tipo de dados construído, como mostrado pela ilustração a seguir.

![recursão de terceto TLV de der](images/der-tlv-recursive.png)

Consulte os tópicos a seguir para obter informações detalhadas sobre os componentes de um TLV terceto.

-   [Bytes de marca codificados](about-encoded-tag-bytes.md)
-   [Comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos construídos](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



