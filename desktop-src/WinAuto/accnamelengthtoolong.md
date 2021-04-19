---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811590"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Texto

O nome do elemento não deve retornar uma cadeia de caracteres com mais de um {0} caractere

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O nome de um elemento contém muitos caracteres. Por exemplo, o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar o nome MSAA de um elemento retorna uma cadeia de caracteres maior que o limite de 32000 caracteres.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




