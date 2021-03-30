---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637133"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Texto

O nome do elemento ( {0} ) não deve conter o texto da função do elemento ( {1} )

## <a name="type"></a>Type

Aviso

## <a name="description"></a>Descrição

O nome de um elemento incorpora sua função de MSAA ou tipo de controle UIA. Por exemplo, esse aviso pode ocorrer se o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) — que é usado para recuperar o nome de MSAA de um elemento — retorna " \_ barra de rolagem do sistema de função \_ \_ \* ".

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque a função será lida duas vezes, ou pode ser inpronunciada ou não intuitiva para os usuários.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.
-   O elemento ou seu pai tem um nome padrão que não foi revisado para um nome amigável. Por exemplo, Button1.
-   Um desenvolvedor não está ciente de que os leitores de tela lêem nomes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




