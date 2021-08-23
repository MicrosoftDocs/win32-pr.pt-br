---
title: Códigos em FACILITY_ITF
description: Códigos no \_ FACILITY ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2a16d051c352c353376865265c0451014f6110fbcde326914c3cc244a36223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793786"
---
# <a name="codes-in-facility_itf"></a>Códigos no \_ FACILITY ITF

**HRESULT** s com recursos como FACILITY NULL e FACILITY RPC têm significado universal porque são definidos em \_ uma única \_ fonte: Microsoft. No entanto, **HRESULT** s no FACILITY ITF são determinados pela função ou método \_ de interface do qual eles são retornados. Isso significa que o mesmo valor de 32 bits em FACILITY ITF retornado de dois métodos de \_ interface diferentes pode ter significados diferentes.

O motivo pelo qual os **HRESULT** s no FACILITY ITF podem ter significados diferentes em interfaces diferentes é que os HRESULT s são mantidos com um tamanho de tipo de dados eficiente de \_ 32 bits. Infelizmente, 32 bits não são grandes o suficiente para o desenvolvimento de um sistema de alocação de código de erro que evita códigos conflitantes alocados por programadores diferentes em momentos diferentes em locais diferentes (ao contrário do tratamento de identificadores de interface e CLSIDs). Como resultado, o **HRESULT** de 32 bits é estruturado de forma que a Microsoft possa definir vários códigos de erro universais, permitindo que outros programadores definam novos códigos de erro sem medo de conflito. A convenção de código de status é a seguinte:

-   Códigos de status em instalações diferentes do \_ FACILITY ITF podem ser definidos somente pela Microsoft.
-   Os códigos de status no FACILITY ITF são definidos exclusivamente pelo desenvolvedor da interface ou função \_ que retorna o código de status. Para evitar códigos de erro conflitantes, quem define a interface é responsável por coordenar e publicar os códigos de status do FACILITY ITF associados \_ a essa interface.

Todos os códigos DE ITF DE INSTALAÇÃO definidos pelo COM têm um valor de código no \_ intervalo de 0x0000-0x01FF. Embora seja legal usar códigos no FACILITY ITF, é recomendável que somente os valores de código no intervalo de \_ 0x0200-0xFFFF sejam usados. Essa recomendação é feita como um meio de reduzir a confusão com erros definidos pelo COM.

Também é recomendável que os desenvolvedores definam novas funções e interfaces para retornar códigos de erro conforme definido por COM e em instalações diferentes do \_ FACILITY ITF. Em particular, as interfaces que têm qualquer chance de serem remotas usando RPC no futuro devem definir os códigos de RPC facility \_ como legais. E \_ UNEXPECTED é um código de erro específico que a maioria dos desenvolvedores deseja tornar universalmente legal.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

 




