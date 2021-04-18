---
title: Tratamento de erros no COM (introdução ao Win32 e ao C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105796341"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Tratamento de erros no COM (introdução ao Win32 e ao C++)

COM usa valores **HRESULT** para indicar o êxito ou a falha de um método ou uma chamada de função. Vários cabeçalhos de SDK definem várias constantes **HRESULT** . Um conjunto comum de códigos de todo o sistema é definido no WinError. h. A tabela a seguir mostra alguns desses códigos de retorno em todo o sistema.



| Constante            | Valor numérico | Descrição                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSDENIED** | 0x80070005    | Acesso negado.                                       |
| **E \_ falha**         | 0x80004005    | Erro não especificado.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valor de parâmetro inválido.                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | Sem memória.                                       |
| **\_ponteiro E**      | 0x80004003    | **NULL** foi passado incorretamente para um valor de ponteiro. |
| **E \_ inesperado**   | 0x8000FFFF    | Condição inesperada.                                |
| **S \_ OK**           | 0x0           | Êxito.                                             |
| **\_falso**        | 0x1           | Êxito.                                             |



 

Todas as constantes com o prefixo "E \_ " são códigos de erro. As constantes **s \_ OK** e **s \_ false** são códigos de êxito. Provavelmente, 99% dos métodos COM retornarão **S \_ OK** quando forem bem-sucedidos; mas não deixe esse fato enganar. Um método pode retornar outros códigos de êxito e, portanto, sempre testar erros usando a macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) ou [**Failed**](/windows/desktop/api/winerror/nf-winerror-failed) . O código de exemplo a seguir mostra a maneira errada e a maneira correta de testar o êxito de uma chamada de função.


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



O código de sucesso **S \_ false** merece menção. Alguns métodos usam **S \_ false** para significar, aproximadamente, uma condição negativa que não é uma falha. Ele também pode indicar um "não op" — o método foi bem-sucedido, mas não teve nenhum efeito. Por exemplo, a função [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) retornará **S \_ false** se você chamá-la uma segunda vez a partir do mesmo thread. Se você precisar diferenciar entre **s \_ OK** e o **\_ falso** em seu código, você deve testar o valor diretamente, mas ainda assim usar [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) ou com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) para lidar com os casos restantes, conforme mostrado no código de exemplo a seguir.


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



Alguns valores **HRESULT** são específicos de um determinado recurso ou subsistema do Windows. Por exemplo, a API de gráficos do Direct2D define o código de erro **D2DERR \_ \_ \_ formato de pixel sem suporte**, o que significa que o programa usou um formato de pixel sem suporte. A documentação do MSDN geralmente fornece uma lista de códigos de erro específicos que um método pode retornar. No entanto, você não deve considerar essas listas como definitivas. Um método sempre pode retornar um valor **HRESULT** que não esteja listado na documentação. Novamente, use as macros com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) . Se você testar um código de erro específico, inclua também um caso padrão.


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>Padrões para tratamento de erros

Esta seção examina alguns padrões para lidar COM erros de COM de forma estruturada. Cada padrão tem vantagens e desvantagens. Até certo ponto, a escolha é uma questão de gosto. Se você trabalha em um projeto existente, talvez ele já tenha diretrizes de codificação que contratam um estilo específico. Independentemente de qual padrão você adotar, o código robusto obedecerá às regras a seguir.

-   Para cada método ou função que retorna um **HRESULT**, verifique o valor de retorno antes de continuar.
-   Libere os recursos depois que eles forem usados.
-   Não tente acessar recursos inválidos ou não inicializados, como ponteiros **nulos** .
-   Não tente usar um recurso depois de liberá-lo.

Com essas regras em mente, aqui estão quatro padrões para lidar com erros.

-   [IFS aninhado](#nested-ifs)
-   [IFS em cascata](#cascading-ifs)
-   [Falha ao saltar](#jump-on-fail)
-   [Lançar em caso de falha](#throw-on-fail)

### <a name="nested-ifs"></a>IFS aninhado

Depois de cada chamada que retorna um **HRESULT**, use uma instrução **If** para testar o êxito. Em seguida, coloque a próxima chamada de método dentro do escopo da instrução **If** . Mais instruções **If** podem ser aninhadas tão profundamente quanto necessário. Os exemplos de código anteriores neste módulo têm todos usado esse padrão, mas aqui está novamente:


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



Vantagens

-   As variáveis podem ser declaradas com escopo mínimo. Por exemplo, *pItem* não é declarado até que seja usado.
-   Dentro de cada instrução **If** , determinadas invariáveis são verdadeiras: todas as chamadas anteriores foram bem-sucedidas e todos os recursos adquiridos ainda são válidos. No exemplo anterior, quando o programa atinge a instrução **If** mais interna, *pItem* e *pFileOpen* são conhecidos como válidos.
-   Fica claro quando liberar ponteiros de interface e outros recursos. Você libera um recurso no final da instrução **If** que segue imediatamente a chamada que adquiriu o recurso.

Desvantagens

-   Algumas pessoas consideram um aninhamento profundo e difícil de ler.
-   O tratamento de erros é misturado com outras instruções de ramificação e looping. Isso pode tornar a lógica geral do programa mais difícil de seguir.

### <a name="cascading-ifs"></a>IFS em cascata

Depois de cada chamada de método, use uma instrução **If** para testar o sucesso. Se o método tiver sucesso, coloque a próxima chamada de método dentro do bloco **If** . Mas em vez de aninhar instruções **If** adicionais, coloque cada teste subsequente com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) após o bloco **If** anterior. Se qualquer método falhar, todos os testes restantes com **êxito** simplesmente falharão até que a parte inferior da função seja atingida.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Nesse padrão, você libera recursos no final da função. Se ocorrer um erro, alguns ponteiros poderão ser inválidos quando a função for encerrada. Chamar a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em um ponteiro inválido falhará no programa (ou pior), portanto, você deve inicializar todos os ponteiros para **NULL** e verificar se eles são **nulos** antes de liberá-los. Este exemplo usa a `SafeRelease` função; os ponteiros inteligentes também são uma boa opção.

Se você usar esse padrão, deverá ter cuidado com construções de loop. Dentro de um loop, interrompa o loop se qualquer chamada falhar.

Vantagens

-   Esse padrão cria menos aninhamento do que o padrão "IFS aninhado".
-   O fluxo de controle geral é mais fácil de ver.
-   Os recursos são liberados em um ponto no código.

Desvantagens

-   Todas as variáveis devem ser declaradas e inicializadas na parte superior da função.
-   Se uma chamada falhar, a função fará várias verificações de erro desnecessárias, em vez de sair da função imediatamente.
-   Como o fluxo de controle continua pela função após uma falha, você deve ter cuidado ao longo do corpo da função para não acessar recursos inválidos.
-   Os erros dentro de um loop exigem um caso especial.

### <a name="jump-on-fail"></a>Falha ao saltar

Após cada chamada de método, teste a falha (não êxito). Em caso de falha, salte para um rótulo próximo à parte inferior da função. Após o rótulo, mas antes de sair da função, libere os recursos.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Vantagens

-   O fluxo de controle geral é fácil de ver.
-   Em todos os pontos do código após uma verificação [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) , se você não tiver passado para o rótulo, será garantido que todas as chamadas anteriores tenham sido bem-sucedidas.
-   Os recursos são lançados em um único lugar no código.

Desvantagens

-   Todas as variáveis devem ser declaradas e inicializadas na parte superior da função.
-   Alguns programadores não gostam de usar **goto** em seu código. (No entanto, deve-se observar que esse uso de **goto** é altamente estruturado; o código nunca salta para fora da chamada de função atual.)
-   as instruções **goto** ignoram inicializadores.

### <a name="throw-on-fail"></a>Lançar em caso de falha

Em vez de saltar para um rótulo, você pode gerar uma exceção quando um método falhar. Isso pode produzir um estilo mais idiomática de C++ se você estiver acostumado a escrever código de exceção segura.


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



Observe que este exemplo usa a classe **CComPtr** para gerenciar ponteiros de interface. Em geral, se o seu código lançar exceções, você deverá seguir o padrão RAII (aquisição de recurso é inicialização). Ou seja, cada recurso deve ser gerenciado por um objeto cujo destruidor garante que o recurso seja liberado corretamente. Se uma exceção for lançada, a garantia do destruidor será invocada. Caso contrário, seu programa poderá vazar recursos.

Vantagens

-   Compatível com o código existente que usa manipulação de exceção.
-   Compatível com bibliotecas C++ que geram exceções, como a STL (Standard Template Library).

Desvantagens

-   Requer objetos C++ para gerenciar recursos como memória ou identificadores de arquivo.
-   Requer uma boa compreensão de como escrever código de exceção segura.

## <a name="next"></a>Avançar

[Módulo 3. Gráficos do Windows](module-3---windows-graphics.md)

 

 
