---
description: ACEs para controlar o acesso a uma propriedade de objetos
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACEs para controlar o acesso a uma propriedade de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fddd5d78ff5b02bbbe4b9b7a7ce0b77d7be263f9fd3926f44411469af2bb3c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785243"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACEs para controlar o acesso às propriedades de um objeto

A DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) de um objeto de serviço de diretório (DS) pode conter uma hierarquia de ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ), da seguinte maneira:

1.  ACEs que protegem o objeto em si
2.  [ACEs específicas de objeto](object-specific-aces.md) que protegem uma propriedade especificada definida no objeto
3.  ACEs específicas de objeto que protegem uma propriedade especificada no objeto

Nessa hierarquia, os direitos concedidos ou negados em um nível superior se aplicam também aos níveis inferiores. Por exemplo, se uma ACE específica a um objeto em um conjunto de propriedades permitir a confiança do \_ lado \_ direito de ler prop do DS \_ \_ , o objeto de confiança terá acesso de leitura implícito a todas as propriedades do conjunto de propriedades. Da mesma forma, uma ACE no próprio objeto que permite aos anúncios \_ direito de \_ acesso de \_ prop de leitura do DS \_ fornece o acesso de leitura de confiança a todas as propriedades do objeto.

A ilustração a seguir mostra a árvore de um objeto DS hipotético e suas propriedades e conjuntos de propriedade.

![hierarquia de objetos do serviço de diretório](images/accctrl2.png)

Suponha que você deseja permitir o seguinte acesso às propriedades deste objeto DS:

-   Permitir que o grupo tenha uma permissão de leitura/gravação para todas as propriedades do objeto
-   Permitir que todos os outros usuários tenham permissão de leitura/gravação para todas as propriedades, exceto a propriedade D

Para fazer isso, defina as ACEs na DACL do objeto, conforme mostrado na tabela a seguir.



| Confiança  | GUID do objeto    | Tipo de ACE                  | Direitos de acesso                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Grupo A  | Nenhum           | ACE permitida pelo acesso        | ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop |
| Todos | Conjunto de propriedades 1 | ACE de objeto permitido pelo Access | ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop |
| Todos | Propriedade C     | ACE de objeto permitido pelo Access | ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop |



 

A ACE para o grupo A não tem um GUID de objeto, o que significa que ele permite o acesso a todas as propriedades do objeto. A ACE específica do objeto para o conjunto de propriedades 1 permite que todos acessem as propriedades A e B. A outra ACE específica do objeto permite que todos acessem a propriedade C. Observe que, embora essa DACL não tenha nenhuma ACE de acesso negado, ela nega implicitamente o acesso D da propriedade a todos, exceto o grupo A.

Quando um usuário tenta acessar a propriedade de um objeto, o sistema verifica as ACEs, em ordem, até que o acesso solicitado seja explicitamente concedido, negado ou que não haja mais ACEs; nesse caso, o acesso é negado implicitamente.

O sistema avalia:

-   ACEs que se aplicam ao próprio objeto
-   ACEs específicas de objeto que se aplicam ao conjunto de propriedades que contém a propriedade que está sendo acessada
-   ACEs específicas de objeto que se aplicam à propriedade que está sendo acessada

O sistema ignora ACEs específicas de objeto que se aplicam a outras propriedades ou conjuntos de propriedade.

 

 
