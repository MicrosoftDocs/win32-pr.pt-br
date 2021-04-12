---
title: Criando um objeto em COM
description: Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365924"
---
# <a name="creating-an-object-in-com"></a>Criando um objeto em COM

Depois que um thread inicializa a biblioteca COM, é seguro que o thread use interfaces COM. Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.

Em geral, há duas maneiras de criar um objeto COM:

-   O módulo que implementa o objeto pode fornecer uma função projetada especificamente para criar instâncias desse objeto.
-   Como alternativa, COM fornece uma função de criação genérica chamada [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Por exemplo, pegue o objeto hipotético `Shape` do tópico [o que é uma interface com?](what-is-a-com-interface-.md). Nesse exemplo, o `Shape` objeto implementa uma interface chamada `IDrawable` . A biblioteca de gráficos que implementa o `Shape` objeto pode exportar uma função com a assinatura a seguir.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Dada essa função, você pode criar um novo `Shape` objeto da seguinte maneira.


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



O parâmetro *ppShape* é do tipo ponteiro para ponteiro para `IDrawable` . Se você ainda não viu esse padrão antes, a dupla indireção pode ser enigmático.

Considere os requisitos da `CreateShape` função. A função deve dar um `IDrawable` ponteiro de volta ao chamador. Mas o valor de retorno da função já é usado para o código de erro/êxito. Portanto, o ponteiro deve ser retornado por meio de um argumento para a função. O chamador passará uma variável do tipo `IDrawable*` para a função e a função substituirá essa variável por um novo `IDrawable` ponteiro. No C++, há apenas duas maneiras de uma função substituir um valor de parâmetro: passagem por referência ou passagem por endereço. COM usa o segundo, passagem por endereço. E o endereço de um ponteiro é um ponteiro para ponteiro, portanto, o tipo de parâmetro deve ser `IDrawable**` .

Aqui está um diagrama para ajudar a visualizar o que está acontecendo.

![diagrama que mostra o indireção de ponteiro duplo](images/com03.png)

A `CreateShape` função usa o endereço de *pShape* ( `&pShape` ) para gravar um novo valor de ponteiro em *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: uma maneira genérica de criar objetos

A função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornece um mecanismo genérico para a criação de objetos. Para entender **CoCreateInstance**, tenha em mente que dois objetos com podem implementar a mesma interface e um objeto pode implementar duas ou mais interfaces. Assim, uma função genérica que cria objetos precisa de duas informações.

-   Qual objeto criar.
-   Qual interface deve ser obtida do objeto.

Mas como podemos indicar essas informações quando chamamos a função? No COM, um objeto ou uma interface é identificado atribuindo-o um número de 128 bits, chamado de GUID ( *identificador global exclusivo* ). Os GUIDs são gerados de forma a torná-los efetivamente exclusivos. Os GUIDs são uma solução para o problema de como criar identificadores exclusivos sem uma autoridade de registro central. Os GUIDs são, às vezes, chamados de UUIDs ( *identificadores universalmente exclusivos* ). Antes do COM, eles eram usados em DCE/RPC (chamada de procedimento remoto/ambiente de computação distribuído). Existem vários algoritmos para criar novos GUIDs. Nem todos esses algoritmos garantem estritamente a exclusividade, mas a probabilidade de criar acidentalmente o mesmo valor de GUID duas vezes é extremamente pequena – efetivamente zero. GUIDs podem ser usados para identificar qualquer tipo de entidade, não apenas objetos e interfaces. No entanto, esse é o único uso que se refere a nós neste módulo.

Por exemplo, a `Shapes` biblioteca pode declarar duas constantes de GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Você pode assumir que os valores numéricos reais de 128 bits para essas constantes estão definidos em outro lugar.) A **\_ forma de CLSID** de constante identifica o `Shape` objeto, enquanto **o \_ IDrawable de IID** constante identifica a `IDrawable` interface. O prefixo "CLSID" significa *identificador de classe* e o *IID* de prefixo significa *identificador de interface*. Essas são convenções de nomenclatura padrão no COM.

Considerando esses valores, você criaria uma nova `Shape` instância da seguinte maneira:


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



A função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tem cinco parâmetros. O primeiro e o quarto parâmetros são o identificador de classe e o identificador de interface. Na verdade, esses parâmetros informam a função "criar o objeto Shape e me dar um ponteiro para a interface IDrawable".

Defina o segundo parâmetro como **NULL**. (Para obter mais informações sobre o significado desse parâmetro, consulte o tópico [agregação](/windows/desktop/com/aggregation) na documentação com.) O terceiro parâmetro usa um conjunto de sinalizadores cujo principal objetivo é especificar o *contexto de execução* para o objeto. O contexto de execução especifica se o objeto é executado no mesmo processo que o aplicativo; em um processo diferente no mesmo computador; ou em um computador remoto. A tabela a seguir mostra os valores mais comuns para esse parâmetro.



| Sinalizador                       | Descrição                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_servidor CLSCTX InProc \_** | Mesmo processo.                                                                                                                                                      |
| **\_servidor local \_ CLSCTX**  | Processo diferente, o mesmo computador.                                                                                                                                  |
| **\_servidor remoto \_ CLSCTX** | Computador diferente.                                                                                                                                                |
| **CLSCTX \_ tudo**            | Use a opção mais eficiente para a qual o objeto dá suporte. (A classificação, da mais eficiente ao menos eficiente, é: em processo, fora do processo e entre computadores.) |



 

A documentação de um componente específico pode informar a qual contexto de execução o objeto dá suporte. Caso contrário, use **CLSCTX \_ All**. Se você solicitar um contexto de execução ao qual o objeto não oferece suporte, a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retornará o código de erro **REGDB \_ E \_ CLASSNOTREG**. Esse código de erro também pode indicar que o CLSID não corresponde a nenhum componente registrado no computador do usuário.

O quinto parâmetro para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recebe um ponteiro para a interface. Como **CoCreateInstance** é um mecanismo genérico, esse parâmetro não pode ser fortemente tipado. Em vez disso, o tipo de dados é **void \* \*** e o chamador deve forçar o endereço do ponteiro para um **tipo \* \* void** . Essa é a finalidade da **\_ conversão de reinterpretação** no exemplo anterior.

É crucial verificar o valor de retorno de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Se a função retornar um código de erro, o ponteiro de interface COM é inválido e a tentativa de desreferenciá-lo pode fazer com que o programa falhe.

Internamente, a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa várias técnicas para criar um objeto. No caso mais simples, ele pesquisa o identificador de classe no registro. A entrada do registro aponta para uma DLL ou EXE que implementa o objeto. **CoCreateInstance** também pode usar informações de um catálogo com+ ou de um manifesto lado a lado (SXS). Independentemente, os detalhes são transparentes para o chamador. Para obter mais informações sobre os detalhes internos de **CoCreateInstance**, consulte [clientes e servidores com](/windows/desktop/com/com-clients-and-servers).

O `Shapes` exemplo que estamos usando é um pouco forçado, então agora vamos voltar a um exemplo do mundo real de com em ação: exibindo a caixa de diálogo **abrir** para o usuário selecionar um arquivo.

## <a name="next"></a>Avançar

[Exemplo: a caixa de diálogo abrir](example--the-open-dialog-box.md)

 

 