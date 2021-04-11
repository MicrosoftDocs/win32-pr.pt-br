---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292244"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Texto

A variante retornada de {0} deve ser um {1} , mas é um {2} .

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento está relatando uma função de MSAA inválida. Por exemplo, o método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) usado para recuperar a função MSAA de um elemento deve retornar um valor inteiro que representa uma das constantes da função MSAA, mas que está retornando outra variante em vez disso.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque os elementos podem ser identificados incorretamente para o usuário.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem uma função de MSAA definida incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Funções de objeto**](object-roles.md)
</dt> </dl>

 

 




