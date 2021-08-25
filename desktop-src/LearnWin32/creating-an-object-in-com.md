---
title: Criando um objeto em COM
description: Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e15874e1d4dcb6bc29fad90f40f90b478c805ccc7b0d0085f560a8b56e2247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913757"
---
# <a name="creating-an-object-in-com"></a>Criando um objeto em COM

Depois que um thread tiver inicializado a biblioteca COM, é seguro para o thread usar interfaces COM. Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.

Em geral, há duas maneiras de criar um objeto COM:

-   O módulo que implementa o objeto pode fornecer uma função especificamente projetada para criar instâncias desse objeto.
-   Como alternativa, o COM fornece uma função de criação genérica chamada [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Por exemplo, pegue o objeto `Shape` hipotético do tópico [O que é uma interface COM?](what-is-a-com-interface-.md). Nesse exemplo, o `Shape` objeto implementa uma interface chamada `IDrawable` . A biblioteca de elementos gráficos que implementa o `Shape` objeto pode exportar uma função com a assinatura a seguir.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Dada essa função, você pode criar um `Shape` novo objeto da seguinte forma.


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



O *parâmetro ppShape* é do tipo pointer-to-pointer-to- `IDrawable` . Se você não tiver visto esse padrão antes, a indronização dupla poderá ser uma indemação.

Considere os requisitos da `CreateShape` função. A função deve retornar `IDrawable` um ponteiro para o chamador. Mas o valor de retorno da função já é usado para o código de erro/êxito. Portanto, o ponteiro deve ser retornado por meio de um argumento para a função. O chamador passará uma variável do tipo para a função e a função substituirá essa variável `IDrawable*` por um novo `IDrawable` ponteiro. No C++, há apenas duas maneiras para uma função substituir um valor de parâmetro: passar por referência ou passar por endereço. COM usa o último, passagem por endereço. E o endereço de um ponteiro é um ponteiro para um ponteiro, portanto, o tipo de parâmetro deve ser `IDrawable**` .

Aqui está um diagrama para ajudar a visualizar o que está acontecendo.

![diagrama que mostra a indionação de ponteiro duplo](images/com03.png)

A `CreateShape` função usa o endereço de *pShape* ( `&pShape` ) para gravar um novo valor de ponteiro em *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: uma maneira genérica de criar objetos

A [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornece um mecanismo genérico para criar objetos. Para entender **CoCreateInstance**, tenha em mente que dois objetos COM podem implementar a mesma interface e um objeto pode implementar duas ou mais interfaces. Portanto, uma função genérica que cria objetos precisa de duas informações.

-   Qual objeto criar.
-   Qual interface obter do objeto.

Mas como indicamos essas informações quando chamamos a função? No COM, um objeto ou uma interface é identificado atribuindo a ele um número de 128 bits, chamado de GUID *(identificador global* exclusivo). GUIDs são gerados de uma maneira que os torna efetivamente exclusivos. GUIDs são uma solução para o problema de como criar identificadores exclusivos sem uma autoridade de registro central. Às vezes, os GUIDs são chamados de UUIDs *(identificadores* universalmente exclusivos). Antes do COM, eles eram usados em DCE/RPC (Distributed Computing Environment/Remote Procedure Call). Existem vários algoritmos para criar novos GUIDs. Nem todos esses algoritmos garantem estritamente a exclusividade, mas a probabilidade de criar acidentalmente o mesmo valor guid duas vezes é extremamente pequena, efetivamente zero. GUIDs podem ser usados para identificar qualquer tipo de entidade, não apenas objetos e interfaces. No entanto, esse é o único uso que nos preocupa neste módulo.

Por exemplo, a `Shapes` biblioteca pode declarar duas constantes GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Você pode supor que os valores numéricos reais de 128 bits para essas constantes são definidos em outro lugar.) A forma **CLSID constante \_** identifica o objeto, enquanto `Shape` a constante **\_ IID IDrawable** identifica a `IDrawable` interface. O prefixo "CLSID" significa *identificador de* classe e o *prefixo IID* significa *identificador de interface*. Essas são convenções de nomen por padrão no COM.

Considerando esses valores, você criaria uma nova `Shape` instância da seguinte forma:


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



A [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tem cinco parâmetros. O primeiro e o quarto parâmetros são o identificador de classe e o identificador de interface. Na verdade, esses parâmetros dizem à função "Criar o objeto Shape e me dê um ponteiro para a interface IDrawable".

De definir o segundo parâmetro como **NULL.** (Para obter mais informações sobre o significado desse parâmetro, consulte o tópico [Agregação](/windows/desktop/com/aggregation) na documentação COM.) O terceiro parâmetro aceita um conjunto de sinalizadores cuja principal finalidade é especificar o *contexto de execução* para o objeto . O contexto de execução especifica se o objeto é executado no mesmo processo que o aplicativo; em um processo diferente no mesmo computador; ou em um computador remoto. A tabela a seguir mostra os valores mais comuns para esse parâmetro.



| Sinalizador                       | Descrição                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX \_ INPROC \_ SERVER** | Mesmo processo.                                                                                                                                                      |
| **SERVIDOR LOCAL CLSCTX \_ \_**  | Processo diferente, mesmo computador.                                                                                                                                  |
| **SERVIDOR REMOTO \_ CLSCTX \_** | Computador diferente.                                                                                                                                                |
| **CLSCTX \_ ALL**            | Use a opção mais eficiente à qual o objeto dá suporte. (A classificação, do mais eficiente ao menos eficiente, é: em processo, fora de processo e entre computadores.) |



 

A documentação de um componente específico pode lhe dizer a qual contexto de execução o objeto dá suporte. Caso não, use **CLSCTX \_ ALL.** Se você solicitar um contexto de execução ao qual o objeto não dá suporte, a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retornará o código de erro **REGDB \_ E \_ CLASSNOTREG**. Esse código de erro também pode indicar que o CLSID não corresponde a nenhum componente registrado no computador do usuário.

O quinto parâmetro para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recebe um ponteiro para a interface . Como **CoCreateInstance é** um mecanismo genérico, esse parâmetro não pode ser fortemente digitado. Em vez disso, o tipo de dados é **nulo \* \*** e o chamador deve coerção do endereço do ponteiro para um **tipo \* \* nulo.** Essa é a finalidade da **reinterpretação \_ de cast** no exemplo anterior.

É crucial verificar o valor de retorno de [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Se a função retornar um código de erro, o ponteiro da interface COM será inválido e a tentativa de desreferenciar poderá causar falha no programa.

Internamente, a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa várias técnicas para criar um objeto . No caso mais simples, ele procura o identificador de classe no Registro. A entrada do Registro aponta para uma DLL ou EXE que implementa o objeto . **CoCreateInstance** também pode usar informações de um catálogo COM+ ou um manifesto lado a lado (SxS). Independentemente disso, os detalhes são transparentes para o chamador. Para obter mais informações sobre os detalhes internos do **CoCreateInstance,** consulte [Clientes e servidores COM.](/windows/desktop/com/com-clients-and-servers)

O exemplo que estamos usando é um pouco artificial, portanto, agora vamos nos voltar para um exemplo real de COM em ação: exibindo a caixa de diálogo Abrir para o usuário selecionar `Shapes` um arquivo. 

## <a name="next"></a>Avançar

[Exemplo: a caixa de diálogo Abrir](example--the-open-dialog-box.md)

 

 