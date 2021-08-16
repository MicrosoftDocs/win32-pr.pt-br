---
title: O atributo represent_as
description: O atributo \ representa \_ como \ permite que você especifique como um tipo de dados transmititable específico é representado ao aplicativo.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, atributos represent_as de chamada de procedimento remoto
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbf217260f3d23f7390a2295d7db5a36174ae01a94f7368f8e7d2085d19ae0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923995"
---
# <a name="the-represent_as-attribute"></a>O atributo de representar \_ como

O \[ atributo " [representar \_ como](/windows/desktop/Midl/represent-as) " \] permite especificar como um tipo de dados de transmissão específico é representado ao aplicativo. Isso é feito especificando o nome do tipo representado para um tipo de transmissões conhecido e fornecendo as rotinas de conversão. Você também deve fornecer as rotinas para liberar a memória usada pelos objetos de tipo de dados.

Use o atributo " **\[ representar \_ como \]** " para apresentar um aplicativo com um tipo de dados diferente, possivelmente não transmitido, em vez do tipo que é realmente transmitido entre o cliente e o servidor. Também é possível que o tipo manipulado pelo aplicativo possa ser desconhecido no momento da compilação MIDL. Quando você escolhe um tipo de transmissãotable bem definido, não precisa se preocupar com a representação de dados no ambiente heterogêneo. O atributo " **\[ representar \_ como \]** " pode tornar seu aplicativo mais eficiente, reduzindo a quantidade de dados transmitidos pela rede.

O atributo **\[ representar \_ \] como** é semelhante ao atributo \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] . No entanto, embora a **\[ transmissão \_ como \]** permita que você especifique um tipo de dados que será usado para transmissão, **\[ represente \_ como \]** permite especificar como um tipo de dados é representado para o aplicativo. O tipo representado não precisa ser definido nos arquivos de MIDL processados; Ele pode ser definido no momento em que os stubs são compilados com o compilador C. Para fazer isso, use a diretiva include no [arquivo de configuração de aplicativo (ACF)](the-application-configuration-file-acf-.md) para compilar o arquivo de cabeçalho apropriado. Por exemplo, o ACF a seguir define um tipo local para o aplicativo **, \_ tipo repr**, para o tipo nomeado de transmittable **\_ :**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

A tabela a seguir descreve as quatro rotinas fornecidas pelo programador.



| Rotina                      | Description                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **\_tipo nomeado \_ do \_ local** | Aloca uma instância do tipo de rede e converte do tipo local para o tipo de rede.      |
| **\_tipo nomeado \_ para \_ local**   | Converte o tipo de rede para o tipo local.                                                    |
| **\_tipo nomeado \_ \_ local gratuito** | Libera a memória alocada por uma chamada para **o \_ tipo nomeado para a rotina \_ \_ local** , mas não para o próprio tipo. |
| **Inst. de \_ tipo nomeado \_ \_**  | Libera o armazenamento para o tipo de rede (ambos os lados).                                                     |



 

Além dessas quatro rotinas fornecidas pelo programador, o tipo nomeado não é manipulado pelo aplicativo. O único tipo visível para o aplicativo é o tipo representado. O aplicativo usa o nome do tipo representado em vez do nome do tipo transmitido nos protótipos e stubs gerados pelo compilador. Você deve fornecer o conjunto de rotinas para ambos os lados.

Para objetos **de \_ tipo nomeado** temporário, o stub chamará o **\_ tipo nomeado \_ \_ Inst gratuitamente** para liberar qualquer memória alocada por uma chamada para o **\_ tipo nomeado \_ de \_ local**.

Se o tipo representado for um ponteiro ou contiver um ponteiro, **o \_ tipo nomeado \_ para rotina \_ local** deverá alocar memória para os dados aos quais os ponteiros apontam (o próprio objeto de tipo representado é manipulado pelo stub da maneira usual). Para \[ [](/windows/desktop/Midl/out-idl) \] os parâmetros out e \[ [in](/windows/desktop/Midl/in), out \] de um tipo que contém **\[ representar \_ como** ou um de seus componentes, a rotina **\_ \_ \_ local gratuita de tipo nomeado** é chamada automaticamente para os objetos de dados que contêm o atributo. Para parâmetros **\[ in \]** , a **rotina \_ \_ \_ local gratuita de tipo nomeado** será chamada somente se o atributo **\[ representar \_ como \]** tiver sido aplicado ao parâmetro. Se o atributo tiver sido aplicado aos componentes do parâmetro, a rotina *\* *** \_ \_ local * gratuita* não será chamada. As rotinas de liberação não são chamadas para os dados inseridos e para a chamada no máximo uma vez (relacionadas ao atributo de nível superior) para um parâmetro **\[ in \]** only.

> [!Note]  
> É possível aplicar a **\[ transmissão \_ como \]** e **\[ representar \_ como \]** atributos para o mesmo tipo. Ao realizar o marshaling de dados, o **\[ representar \_ como \]** conversão de tipo é aplicado primeiro e, em seguida, a **\[ transmissão \_ como \]** conversão é aplicada. O pedido é invertido ao desempacotar dados. Assim, quando o marshaling, \* *_\_ de \_ local_* aloca uma instância de um tipo nomeado e a traduz de um objeto de tipo local para o objeto de tipo nomeado temporário. Esse objeto é o objeto de tipo apresentado usado para a rotina de \* *_\_ \_ transmissão_* . A \* rotina *_\_ to \_ transmissão_* aloca um objeto de tipo transmitido e o traduz do objeto apresentado (nomeado) para o objeto transmitido.

 

Uma matriz de inteiros longos pode ser usada para representar uma lista vinculada. Dessa forma, o aplicativo manipula a lista e a transmissão usa uma matriz de inteiros longos quando uma lista desse tipo é transmitida. Você pode começar com uma matriz, mas usar uma construção com uma matriz aberta de inteiros longos é mais conveniente. O exemplo a seguir mostra como fazer isso.

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

Observe que os protótipos das rotinas que usam o tipo **LONGARR** são realmente exibidos nos arquivos stub. h como **PLOC \_ Box** no lugar do tipo **LONGARR** . O mesmo é verdadeiro para os stubs apropriados no arquivo de stub \_ c. c.

Você deve fornecer as quatro funções a seguir:

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

As rotinas mostradas acima fazem o seguinte:

-   O **LONGARR \_ da rotina \_ local** conta os nós da lista, aloca um objeto LONGARR com o tamanho de **sizeof**(**LONGARR**) + contagem \* *_sizeof_*(**Long**), define o campo **tamanho** como contagem e copia os dados para o campo **DataArr** .
-   A rotina **LONGARR \_ to \_ local** cria uma lista com nós de tamanho e transfere a matriz para os nós apropriados.
-   A **rotina \_ \_ Inst LONGARR Free** libera nada nesse caso.
-   A **rotina \_ \_ local gratuita LONGARR** libera todos os nós da lista.

 

 