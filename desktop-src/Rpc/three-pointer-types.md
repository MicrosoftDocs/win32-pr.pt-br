---
title: Três tipos de ponteiro
description: O MIDL dá suporte a três tipos de ponteiros para acomodar uma ampla gama de aplicativos.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9627c71b07c86ab2deb7e28bddcf6d30b1747cf7d44874620f4053383a5a948a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923455"
---
# <a name="three-pointer-types"></a>Três tipos de ponteiro

O MIDL dá suporte a três tipos de ponteiros para acomodar uma ampla gama de aplicativos. Os três níveis diferentes são chamados de referência, exclusivos e ponteiros completos, e são indicados pelos atributos **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**Unique**](/windows/desktop/Midl/unique) **\]** e **\[** [**PTR**](/windows/desktop/Midl/ptr) **\]** , respectivamente. As classes de ponteiro descritas por esses atributos são mutuamente exclusivas. Os atributos de ponteiro podem ser aplicados a ponteiros em definições de tipo, tipos de retorno de função, parâmetros de função, membros de estruturas ou uniões ou elementos de matriz.

Ponteiros inseridos são ponteiros que são membros de estruturas ou uniões. Eles também podem ser elementos de matrizes. Na **\[** [](/windows/desktop/Midl/in) **\]** direção, os ponteiros de **\[ referência \]** inseridos são considerados como apontados para um armazenamento válido e não devem ser nulos. Essa situação é aplicável recursivamente a quaisquer ponteiros de **\[ referência \]** aos quais estão apontando. Na direção **\[ , \]** os ponteiros **\[ únicos \]** e completos inseridos (ponteiros com o atributo **\[ PTR \]** ) podem ou não ser nulos.

Qualquer atributo de ponteiro colocado em um parâmetro na sintaxe de uma declaração de função afeta apenas o Declarador de ponteiro mais à direita para esse parâmetro. Para afetar os declaradores de ponteiro, os tipos de nomes intermediários devem ser usados.

As funções que retornam um ponteiro podem ter um atributo de ponteiro como um atributo de função. Os atributos **\[ Unique \]** e **\[ PTR \]** devem ser aplicados aos tipos de retorno de função. Declarações de membro que são ponteiros podem especificar um atributo de ponteiro como um atributo de campo. Um atributo de ponteiro também pode ser aplicado como um atributo de tipo em constructos de [**typedef**](/windows/desktop/Midl/typedef) .

Quando nenhum atributo de ponteiro é especificado como um atributo de campo ou tipo, os atributos de ponteiro são aplicados de acordo com as regras para uma declaração de ponteiro sem atributo, como a seguir.

No modo de compatibilidade com DCE, os atributos de ponteiro são determinados na definição do arquivo IDL. Se houver um atributo **\[** [**\_ padrão de ponteiro**](/windows/desktop/Midl/pointer-default) **\]** especificado na interface de definição, esse atributo será usado. Se nenhum atributo **\[ \_ padrão \] de ponteiro** estiver presente, todos os ponteiros sem atributo serão ponteiros completos.

No modo extensões da Microsoft, os atributos de ponteiro podem ser determinados pela importação de arquivos IDL e são aplicados na seguinte ordem:

1.  Um atributo de ponteiro explícito aplicado ao site de uso.
2.  O atributo **\[ ref \]** , quando o ponteiro sem atributo é um parâmetro de ponteiro de nível superior.
3.  Um atributo **\[ \_ padrão \] de ponteiro** especificado na interface de definição.
4.  Um atributo **\[ \_ padrão \] de ponteiro** especificado na interface base.
5.  O atributo **\[ exclusivo \]** .

O **\[** atributo de interface [**\_ padrão do ponteiro**](/windows/desktop/Midl/pointer-default) **\]** especifica os atributos de ponteiro padrão a serem aplicados a um Declarador de ponteiro em um tipo, parâmetro ou declaração de tipo de retorno quando essa declaração não tem um atributo de ponteiro explícito aplicado a ele. O atributo de interface **\[ \_ padrão \] do ponteiro** não se aplica a um ponteiro de nível superior não atributo de um parâmetro, que é considerado como **\[ ref \]**.

 

 