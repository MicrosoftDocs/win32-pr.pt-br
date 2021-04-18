---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811399"
---
# <a name="accnamecontainsinvalidstring"></a>AccNameContainsInvalidString

## <a name="text"></a>Texto

accName não deve conter a cadeia de caracteres {0}

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O nome de um elemento contém caracteres inválidos (esses caracteres são substituídos por AccChecker). Por exemplo, o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar o nome MSAA de um elemento retorna uma cadeia de caracteres que contém a tabulação, nova linha ou caractere de e comercial.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




