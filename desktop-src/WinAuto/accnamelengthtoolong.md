---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327702"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Texto

O nome do elemento não deve retornar uma cadeia de caracteres maior que o {0} caractere

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O nome de um elemento contém muitos caracteres. Por exemplo, o [**método get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar o nome MSAA de um elemento retorna uma cadeia de caracteres maior que o limite de 32000 caracteres.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação, pois um elemento pode ter um nome não intuitivo e imparável.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




