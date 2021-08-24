---
title: Navegação por meio de testes de acerto e localização da tela
description: Para localizar os filhos de um objeto ou determinar o tamanho de um objeto, os clientes podem atingir pontos de teste na tela.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34911b13a4c9bad2bfd79cb32d5654265878568ad00475ade08a87a23150b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828264"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navegação por meio de testes de acerto e localização da tela

Para localizar os filhos de um objeto ou determinar o tamanho de um objeto, os clientes podem atingir pontos de teste na tela. Dois métodos estão disponíveis:

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Usando IAccessible::accHitTest

Para identificar se um ponto está dentro de um objeto, dentro de seu filho ou nenhum deles, os clientes chamam o método [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) do objeto pai, passando as coordenadas de tela do ponto a ser testado. A lista a seguir descreve alguns cenários típicos:

-   Se os filhos do objeto se sobrepõem em um ponto especificado, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera o filho mais alto que aparece visualmente para ocupar o espaço.
-   Se uma janela abranger um filho ou se o filho for recortado pelo pai, o teste de impacto do ponto coberto recuperará o filho mesmo que ele não seja visível.
-   Se o filho encontrado no ponto especificado for um objeto acessível, em vez de um elemento filho, o método retornará a interface [**IDispatch do**](idispatch-interface.md) filho.

## <a name="using-iaccessibleacclocation"></a>Usando IAccessible::accLocation

Para obter o local da tela de um objeto ou um dos filhos do objeto, os clientes chamam [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Esse método retorna as coordenadas do retângulo delimitado do objeto especificado. Se o objeto não for formato como um retângulo, o método retornará as coordenadas do menor retângulo que abrange todo o objeto.

A ilustração a seguir mostra a relação entre a região não retangular de um objeto e seu retângulo delimitador.

![ilustração mostrando a região de um objeto não retangular (um círculo) e seu retângulo delimitador.](images/region.gif)

> [!Note]  
> [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) é mais preciso do que [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque permite que os clientes determinem o local dos objetos em uma base pixel a pixel, em vez de com retângulos delimitadores. Essa precisão é útil, por exemplo, quando um aplicativo está coletando informações acompanhando o local do ponteiro do mouse.

 

 

 




