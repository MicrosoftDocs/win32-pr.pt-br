---
title: Códigos em FACILITY_ITF
description: Códigos no FACILITy \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916107"
---
# <a name="codes-in-facility_itf"></a>Códigos no FACILITy \_ ITF

**HRESULT** s com instalações como a instalação \_ nula e o \_ RPC de instalação têm um significado universal porque eles são definidos em uma única fonte: Microsoft. No entanto, **HRESULT** s no recurso \_ ITF são determinados pelo método de função ou de interface do qual eles são retornados. Isso significa que o mesmo valor de 32 bits no recurso \_ ITF retornado de dois métodos de interface diferentes pode ter significados diferentes.

O motivo pelo qual o **HRESULT** s no recurso \_ ITF pode ter significados diferentes em interfaces diferentes é que **HRESULT** s é mantido para um tamanho de tipo de dados eficiente de 32 bits. Infelizmente, 32 bits não é grande o suficiente para o desenvolvimento de um sistema de alocação de código de erro que evita códigos conflitantes alocados por programadores diferentes em momentos diferentes em locais diferentes (ao contrário da manipulação de identificadores de interface e CLSIDs). Como resultado, o **HRESULT** de 32 bits é estruturado de forma que a Microsoft possa definir vários códigos de erro universal, permitindo que outros programadores definam novos códigos de erro sem medo de conflito. A Convenção de código de status é a seguinte:

-   Os códigos de status em instalações diferentes do recurso \_ ITF podem ser definidos somente pela Microsoft.
-   Os códigos de status no recurso de instalação \_ ITF são definidos exclusivamente pelo desenvolvedor da interface ou função que retorna o código de status. Para evitar códigos de erro conflitantes, qualquer pessoa que define a interface é responsável por coordenar e publicar os \_ códigos de status ITF de instalação associados a essa interface.

Todos os códigos de ITF de instalações definidos COM \_ têm um valor de código no intervalo de 0x0000-0x01FF. Embora seja legal usar qualquer código no recurso \_ ITF, é recomendável que apenas os valores de código no intervalo de 0x0200-0xFFFF sejam usados. Essa recomendação é feita como um meio de reduzir a confusão com erros definidos COM.

Também é recomendável que os desenvolvedores definam novas funções e interfaces para retornar códigos de erro, conforme definido pelo COM e em instalações diferentes do recurso \_ ITF. Em particular, as interfaces que têm qualquer chance de serem remotas usando RPC no futuro devem definir os códigos de RPC do recurso \_ como válidos. E \_ inesperado é um código de erro específico que a maioria dos desenvolvedores deseja tornar universalmente legal.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

 




