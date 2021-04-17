---
title: Navegação por meio de teste de clique e local da tela
description: Para localizar os filhos de um objeto ou para determinar o tamanho de um objeto, os clientes podem clicar em pontos de teste na tela.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755875"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navegação por meio de teste de clique e local da tela

Para localizar os filhos de um objeto ou para determinar o tamanho de um objeto, os clientes podem clicar em pontos de teste na tela. Dois métodos estão disponíveis:

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Usando IAccessible:: accHitTest

Para identificar se um ponto está dentro de um objeto, dentro de seu filho ou nenhum deles, os clientes chamam o método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) do objeto pai, passando as coordenadas da tela do ponto a ser testado. A lista a seguir descreve alguns cenários típicos:

-   Se os filhos do objeto se sobrepõem em um ponto especificado, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera o filho superior que parece Visual ocupar o espaço.
-   Se uma janela abranger um filho ou se o filho for recortado pelo pai, o teste de clique no ponto coberto recuperará o filho mesmo que ele não esteja visível.
-   Se o filho encontrado no ponto especificado for um objeto acessível, em oposição a um elemento filho, o método retornará a interface [**IDispatch**](idispatch-interface.md) do filho.

## <a name="using-iaccessibleacclocation"></a>Usando IAccessible:: accLocation

Para obter o local da tela de um objeto ou de um dos filhos do objeto, os clientes chamam [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Esse método retorna as coordenadas do retângulo delimitador do objeto especificado. Se o objeto não estiver formatado como um retângulo, o método retornará as coordenadas do menor retângulo que abrange todo o objeto.

A ilustração a seguir mostra a relação entre a região não retangular de um objeto e seu retângulo delimitador.

![ilustração mostrando a região de um objeto não retangular (um círculo) e seu retângulo delimitador.](images/region.gif)

> [!Note]  
> [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) é mais preciso que [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque permite que os clientes determinem o local de objetos em um pixel por pixel em vez de com retângulos delimitadores. Essa precisão é útil, por exemplo, quando um aplicativo está coletando informações rastreando o local do ponteiro do mouse.

 

 

 




