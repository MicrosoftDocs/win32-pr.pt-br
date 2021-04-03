---
title: Modificando as interfaces de usuário existentes
description: O painel de resultados do snap-in Active Directory usuários e computadores do MMC exibe várias colunas de dados de atributo para objetos dentro de um contêiner, como os atributos Name e Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modificando o AD de interfaces de usuário existentes
- Snap-in de usuários e computadores AD, modificando a exibição
- Snap-in de usuários e computadores AD, adicionando colunas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822263"
---
# <a name="modifying-existing-user-interfaces"></a>Modificando as interfaces de usuário existentes

O painel de resultados do snap-in Active Directory usuários e computadores do MMC exibe várias colunas de dados de atributo para objetos dentro de um contêiner, como os atributos **Name** e **Description** . O snap-in permite que o usuário adicione e remova as colunas exibidas no painel de resultados do snap-in do.

Para alterar a exibição, o usuário usa o menu suspenso **Exibir** e seleciona **Adicionar/remover colunas**. Na caixa de diálogo **Adicionar/remover colunas** , há uma lista de colunas que o usuário pode escolher para exibir no painel de resultados.

O snap-in Active Directory usuários e computadores do MMC que está incluído no Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition, fornece a capacidade de modificar a lista de colunas que podem ser exibidas no painel de resultados do snap-in para um contêiner. Esse recurso só existe se o snap-in for direcionado a uma floresta com o esquema do Windows Server 2003.

Para adicionar uma coluna à lista, adicione um valor ao atributo **extraColumns** do especificador de exibição para o tipo de objeto ao qual o atributo está associado. O atributo **extraColumns** é um atributo de cadeia de caracteres com valores múltiplos, em que cada cadeia de caracteres está no formato a seguir.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



A tabela a seguir lista o conteúdo desses valores.



| Valor                        | Descrição                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapDisplayName &gt; "    | Contém uma cadeia de caracteres que representa o **ldapDisplayName** do atributo.                                                         |
| " &lt; cabeçalho da coluna &gt; "      | Contém uma cadeia de caracteres que representa o texto exibido no cabeçalho da coluna.                                                  |
| " &lt; visibilidade padrão &gt; " | Contém um valor numérico que será 0 se o atributo estiver oculto por padrão ou 1 se o atributo estiver visível por padrão.               |
| " &lt; largura &gt; "              | Contém a largura da coluna, em pixels. Se esse valor for-1, a largura da coluna será definida com a largura do cabeçalho da coluna. |
| " &lt; não utilizado &gt; "             | Não utilizado. Deve ser zero.                                                                                                               |



 

Por exemplo, para adicionar uma coluna que exibirá o nome canônico de objetos em uma unidade organizacional, um valor para o atributo **canôniconame** será adicionado ao atributo **extraColumns** do objeto de **exibição OrganizationalUnit** no contêiner exibir especificadores. A cadeia de caracteres adicionada ao atributo **extraColumns** do objeto de **exibição OrganizationalUnit** será semelhante ao seguinte.


```C++
canonicalName,Canonical Name,0,150,0
```



A caixa de diálogo **Adicionar/remover colunas** exibe somente as colunas contidas no atributo **ExtraColumns** do objeto **displaySpecifier** do tipo de contêiner que está sendo exibido. Se o atributo **extraColumns** não contiver nenhum valor, a caixa de diálogo **Adicionar/remover colunas** exibirá um conjunto fixo de colunas. Uma cópia do conjunto fixo de colunas está contida no atributo **extraColumns** do objeto de **exibição padrão** .

Para adicionar uma ou mais colunas à lista de colunas de um objeto específico, você deve copiar todos os valores de **extraColumns** do objeto de **exibição padrão** para o objeto de destino e, em seguida, adicionar as colunas personalizadas. Se você especificar o atributo **extraColumns** em uma determinada classe, essa classe usará essas colunas e não as mesclará com as colunas especificadas na classe de **exibição padrão** . Portanto, outras alterações na classe de **exibição padrão** não terão nenhum efeito sobre esse objeto.

Para exibir uma coluna personalizada para todos os tipos de contêiner que não têm nenhuma coluna personalizada registrada, adicione um valor para a coluna ao atributo **extraColumns** do objeto de **exibição padrão** .

 

 




