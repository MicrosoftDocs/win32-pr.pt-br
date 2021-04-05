---
title: Práticas de codificação COM
description: Este tópico descreve maneiras de tornar seu código COM mais eficiente e robusto.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084962"
---
# <a name="com-coding-practices"></a>Práticas de codificação COM

Este tópico descreve maneiras de tornar seu código COM mais eficiente e robusto.

-   [O \_ \_ operador uuidof](/windows)
-   [A \_ macro IID PPV \_ args](/windows)
-   [O padrão SafeRelease](#the-saferelease-pattern)
-   [Ponteiros inteligentes COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>O \_ \_ operador uuidof

Ao compilar seu programa, você pode obter erros de vinculador semelhantes ao seguinte:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Esse erro significa que uma constante GUID foi declarada com ligação externa (**externa**) e o vinculador não pôde localizar a definição da constante. O valor de uma constante de GUID geralmente é exportado de um arquivo de biblioteca estático. Se você estiver usando Microsoft Visual C++, poderá evitar a necessidade de vincular uma biblioteca estática usando o operador **\_ \_ uuidof** . Esse operador é uma extensão de idioma da Microsoft. Ele retorna um valor GUID de uma expressão. A expressão pode ser um nome de tipo de interface, um nome de classe ou um ponteiro de interface. Usando o **\_ \_ uuidof**, você pode criar o objeto de caixa de diálogo de item comum da seguinte maneira:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



O compilador extrai o valor de GUID do cabeçalho, portanto, nenhuma exportação de biblioteca é necessária.

> [!Note]  
> O valor de GUID é associado ao nome do tipo declarando `__declspec(uuid( ... ))` no cabeçalho. Para obter mais informações, consulte a documentação do **\_ \_ declspec** na documentação do Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>A \_ macro IID PPV \_ args

Vimos que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) exigem a coerção do parâmetro final para um tipo **void \* \*** . Isso cria o potencial para uma incompatibilidade de tipo. Considere o fragmento de código a seguir:


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Esse código solicita a interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , mas passa um ponteiro [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . A expressão de **\_ conversão de reinterpretação** evita o sistema de tipos C++, portanto, o compilador não capturará esse erro. Na melhor das hipóteses, se o objeto não implementar a interface solicitada, a chamada simplesmente falhará. Na pior das hipóteses, a função é bem sucedido e você tem um ponteiro incompatível. Em outras palavras, o tipo de ponteiro não corresponde à vtable real na memória. Como você pode imaginar, nada bom pode acontecer nesse ponto.

> [!Note]  
> Uma *vtable* (tabela de método virtual) é uma tabela de ponteiros de função. A vtable é como o COM associa uma chamada de método à sua implementação em tempo de execução. Não coincidentemente, as vtables são como a maioria dos compiladores C++ implementam métodos virtuais.

 

A macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ajuda a evitar essa classe de erro. Para usar essa macro, substitua o código a seguir:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



por este:


```C++
IID_PPV_ARGS(&pFileOpen)
```



A macro é inserida automaticamente `__uuidof(IFileOpenDialog)` para o identificador de interface, portanto, é garantido que ela corresponda ao tipo de ponteiro. Este é o código modificado (e correto):


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Você pode usar a mesma macro com [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>O padrão SafeRelease

A contagem de referência é uma das coisas na programação que é basicamente fácil, mas também é entediante, o que torna mais fácil ficar errado. Os erros típicos incluem:

-   Falha ao liberar um ponteiro de interface quando você terminar de usá-lo. Essa classe de bug fará com que o programa vazasse memória e outros recursos, porque os objetos não são destruídos.
-   Chamando a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) com um ponteiro inválido. Por exemplo, esse erro pode ocorrer se o objeto nunca foi criado. Essa categoria de bug provavelmente causará falha no seu programa.
-   A desreferência de um ponteiro de interface após a [**liberação**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) é chamada. Esse bug pode fazer com que o programa falhe. Pior, pode fazer com que seu programa falhe em um momento aleatório, o que dificulta o rastreamento do erro original.

Uma maneira de evitar esses bugs é chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) por meio de uma função que libera com segurança o ponteiro. O código a seguir mostra uma função que faz isso:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Essa função usa um ponteiro de interface COM como um parâmetro e faz o seguinte:

1.  Verifica se o ponteiro é **nulo**.
2.  Chama a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se o ponteiro não for **nulo**.
3.  Define o ponteiro como **nulo**.

Aqui está um exemplo de como usar `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Se [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) for executado com sucesso, a chamada para `SafeRelease` liberar o ponteiro. Se **CoCreateInstance** falhar, *PFileOpen* permanecerá **nulo**. A `SafeRelease` função verifica isso e ignora a chamada para [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

Também é seguro chamar `SafeRelease` mais de uma vez no mesmo ponteiro, como mostrado aqui:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Ponteiros inteligentes COM

A `SafeRelease` função é útil, mas exige que você se lembre de duas coisas:

-   Inicializar cada ponteiro de interface como **nulo**.
-   Chame `SafeRelease` antes de cada ponteiro sair do escopo.

Como programador de C++, você provavelmente está pensando que não deve ter que se lembrar dessas coisas. Afinal, é por isso que o C++ tem construtores e destruidores. Seria interessante ter uma classe que encapsulasse o ponteiro de interface subjacente, inicializando e liberando automaticamente o ponteiro. Em outras palavras, queremos algo assim:


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



A definição de classe mostrada aqui está incompleta e não pode ser usada como mostrado. No mínimo, você precisaria definir um construtor de cópia, um operador de atribuição e uma maneira de acessar o ponteiro COM subjacente. Felizmente, você não precisa fazer nenhum trabalho, porque Microsoft Visual Studio já fornece uma classe de ponteiro inteligente como parte do Active Template Library (ATL).

A classe de ponteiro inteligente ATL é denominada **CComPtr**. (Há também uma classe **CComQIPtr** , que não é discutida aqui.) Aqui está o exemplo de [caixa de diálogo aberta](example--the-open-dialog-box.md) reescrito para usar **CComPtr**.


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



A principal diferença entre esse código e o exemplo original é que essa versão não chama explicitamente [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Quando a instância **CComPtr** sai do escopo, o destruidor chama **Release** no ponteiro subjacente.

**CComPtr** é um modelo de classe. O argumento de modelo é o tipo de interface COM. Internamente, **CComPtr** mantém um ponteiro desse tipo. **CComPtr** substitui **Operator-> ()** e **operador& ()** para que a classe atue como o ponteiro subjacente. Por exemplo, o código a seguir é equivalente a chamar o método **IFileOpenDialog:: show** diretamente:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** também define um método **CComPtr:: CoCreateInstance** , que chama a função com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com alguns valores de parâmetro padrão. O único parâmetro necessário é o identificador de classe, como mostra o exemplo a seguir:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



O método **CComPtr:: CoCreateInstance** é fornecido puramente como uma conveniência; Você ainda pode chamar a função de [**COCREATEINSTANCE**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com, se preferir.

## <a name="next"></a>Avançar

[Tratamento de erro em COM](error-handling-in-com.md)

 

 