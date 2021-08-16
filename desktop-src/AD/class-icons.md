---
title: Ícones de classe
description: O ícone usado para representar um objeto de classe pode ser especificado no atributo iconPath no contêiner DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nomes de exibição de classe anúncios, ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022597"
---
# <a name="class-icons"></a>Ícones de classe

O ícone usado para representar um objeto de classe pode ser especificado no atributo **iconPath** no contêiner DisplaySpecifiers. Além disso, cada classe pode armazenar vários Estados de ícone. Por exemplo, uma classe de pasta pode ter ícones para os Estados aberto, fechado e desabilitado. A implementação atual aceita um máximo de dezesseis Estados de ícone diferentes por classe.

O atributo **iconPath** pode ser especificado de uma das duas maneiras.


```C++
<state>,<icon file name>
```



ou


```C++
<state>,<module file name>,<resource ID>
```



Nesses exemplos, o " &lt; estado &gt; " é um inteiro com um valor entre 0 e 15. O valor 0 é definido como o estado padrão ou fechado do ícone. O valor 1 é definido para ser o estado aberto do ícone. O valor 2 é o estado desabilitado. Todos os outros valores são definidos pelo aplicativo.

O " &lt; nome do arquivo &gt; de ícone" é o caminho e o nome de arquivo de um arquivo de ícone que contém a imagem do ícone.

O " &lt; nome do arquivo &gt; de módulo" é o caminho e o nome de arquivo de um módulo, como um exe ou dll, que contém a imagem de ícone em um recurso. O " &lt; ID do recurso &gt; " é um inteiro que especifica o identificador de recurso do recurso de ícone dentro do módulo.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Adicionando um valor ao atributo **iconPath**

Para adicionar um valor ao atributo **iconPath** , execute as etapas a seguir.

1.  Determine se o valor do atributo existe. Se um valor for para ser substituído, primeiro exclua o valor existente usando o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **\_ Propriedade ADS \_ delete** e o parâmetro *vProp* definido como o valor a ser removido. Não use a **\_ Propriedade ADS \_ Clear** ou **a \_ \_ atualização da propriedade ADS** para *lnControlCode*.
2.  Crie a cadeia de caracteres que representa os dados de ícone de atributo. Para obter um exemplo, consulte o formato acima.
3.  Para adicionar o novo valor, use o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **propriedade \_ de \_ acréscimo do ADS**.
4.  Para confirmar as alterações no diretório, chame [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 