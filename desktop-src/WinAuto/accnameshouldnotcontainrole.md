---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f09bd9ccdf27c5f52a45466b6b8145cfe23248cc175777f57202aac6530791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899722"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Texto

O Nome do Elemento ( ) não deve conter o texto da {0} Função do Elemento ( {1} )

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

O nome de um elemento incorpora sua função MSAA ou tipo de controle UIA. Por exemplo, esse aviso poderá ocorrer se o método [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , que é usado para recuperar o nome MSAA de um elemento, retornar "ROLE \_ SYSTEM \_ SCROLLBAR \_ \* ".

Esse problema causa problemas para pessoas que dependem de um leitor de tela e teclado para navegação porque a função será lida duas vezes ou pode ser não pronúnciável ou não intuitiva para os usuários.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.
-   O elemento ou seu pai tem um nome padrão que não foi revisado para um nome amigável. Por exemplo, button1.
-   Um desenvolvedor não está ciente de que os leitores de tela leem nomes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




