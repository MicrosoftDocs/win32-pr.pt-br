---
description: Um uso típico para componentes transitivos é preparar um produto para reinstalar o durante uma atualização do sistema.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Usando componentes transitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930252"
---
# <a name="using-transitive-components"></a>Usando componentes transitivos

Um uso típico para componentes transitivos é preparar um produto para reinstalar o durante uma atualização do sistema. O autor do pacote de instalação especifica os componentes que precisam ser trocados durante uma atualização do sistema como tendo o atributo transitiva. Quando o usuário atualizar mais tarde o sistema, o produto deverá ser reinstalado. Após essa reinstalação, o instalador removerá os componentes anteriores e instalará os componentes mais recentes, sem precisar instalar o produto inteiro.

**Para incluir dois componentes transitivos no pacote de instalação**

1.  Inclua os componentes transitivos no pacote de instalação.
2.  Crie componentes transitivos na [tabela](component-table.md) de componentes da mesma forma que os componentes regulares. Cada componente transitivo deve ter seu próprio GUID exclusivo especificado na coluna ComponentID.
3.  Inclua o bit **msidbComponentAttributesTransitive** na coluna Attributes da tabela Component para cada componente transitiva. Se esse bit for definido, o instalador reavaliará o valor da instrução na coluna condição após uma reinstalação.

    Se o valor era falso anteriormente e foi alterado para true, o instalador instalará o componente.

    Se o valor era verdadeiro anteriormente e foi alterado para false, o instalador removerá o componente, mesmo que o componente tenha outros produtos como clientes.

    > [!Note]  
    > A menos que o bit transitiva seja definido, o componente permanece habilitado uma vez instalado, mesmo que a instrução condicional seja avaliada como falsa em uma instalação de manutenção subsequente do produto. As condições devem ser baseadas apenas em Estados de computador. Não use com condições baseadas em Estados do usuário ou propriedades definidas na linha de comando, pois isso pode fazer com que o instalador exija uma reinstalação do produto em cada uso por um usuário diferente.

     

4.  Insira expressões condicionais complementares nos campos de condição da tabela de controle, de modo que, quando a condição no primeiro componente transitivo for alterada para false, a condição no segundo componente transitivo será alterada para verdadeiro. Isso resulta na remoção do primeiro componente e na instalação do segundo componente na reinstalação do aplicativo.

Uma reinstalação do produto é necessária para alternar os componentes transitivos. Portanto, os autores de pacote precisam fornecer aos usuários um método para reinstalar o produto e para definir os modos da propriedade [**REinstallmode**](reinstallmode.md) . Há basicamente três maneiras de disparar a reinstalação:

-   Execute e configure a reinstalação por meio da interface do usuário criando um pacote que usa a [*IU completa*](f-gly.md).
-   Execute a reinstalação da linha de comando usando **msiexec/f** e selecione os modos na lista para a [opção de linha de comando](command-line-options.md) **/f** .
-   Faça com que o aplicativo chame [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) ou [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

O bit só deve ser usado com condições baseadas em Estados de computador. Não use com condições baseadas em Estados do usuário ou propriedades definidas na linha de comando, pois isso pode fazer com que o instalador exija uma reinstalação do produto em cada uso por um usuário diferente.

> [!Note]
> A menos que o bit transitiva na coluna atributos seja definido para um componente, o componente permanecerá habilitado uma vez instalado, mesmo que a instrução condicional na coluna condição seja avaliada como false em uma instalação de manutenção subsequente do produto.
> 
> Na maioria dos casos, se um aplicativo incluir componentes transitivos, Windows Installer exigirá que a origem do aplicativo repare ou atualize o aplicativo. Nesses casos, o CD-ROM de restauração do sistema enviado por um fabricante de equipamento original não funciona e uma fonte de instalação real para o aplicativo precisa ser fornecida.

 

 

 



