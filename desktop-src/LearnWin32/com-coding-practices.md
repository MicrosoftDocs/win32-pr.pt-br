---
title: Práticas de codificação COM
description: Este tópico descreve maneiras de tornar seu código COM mais eficaz e robusto.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93febc4ee3dfd4f05f20fae8078bc2a5ebb7f9623a860f49ec9cd6ce4e69b95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913882"
---
# <a name="com-coding-practices"></a>Práticas de codificação COM

Este tópico descreve maneiras de tornar seu código COM mais eficaz e robusto.

-   [O \_ \_ operador uuidof](/windows)
-   [A macro \_ ARGS IID PPV \_](/windows)
-   [O padrão SafeRelease](#the-saferelease-pattern)
-   [Ponteiros inteligentes COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>O \_ \_ operador uuidof

Ao criar seu programa, você pode receber erros de vinculador semelhantes aos seguintes:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Esse erro significa que uma constante GUID foi declarada com vinculação externa (**extern**) e o linker não pôde encontrar a definição da constante. O valor de uma constante GUID geralmente é exportado de um arquivo de biblioteca estática. Se você estiver usando Microsoft Visual C++, poderá evitar a necessidade de vincular uma biblioteca estática usando o **\_ \_ operador uuidof.** Esse operador é uma extensão de linguagem da Microsoft. Ele retorna um valor GUID de uma expressão. A expressão pode ser um nome de tipo de interface, um nome de classe ou um ponteiro de interface. Usando **\_ \_ uuidof**, você pode criar o objeto Common Item Dialog da seguinte forma:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



O compilador extrai o valor guid do header, portanto, nenhuma exportação de biblioteca é necessária.

> [!Note]  
> O valor guid é associado ao nome do tipo declarando `__declspec(uuid( ... ))` no header. Para obter mais informações, consulte a documentação **\_ \_ para declspec** na documentação Visual C++ dados.

 

## <a name="the-iid_ppv_args-macro"></a>A macro \_ ARGS IID PPV \_

Vimos que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) exigem a coerção do parâmetro final para um **tipo \* \* nulo.** Isso cria o potencial para uma incompatibilidade de tipo. Considere o fragmento de código a seguir:


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



Esse código solicita a interface [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) mas passa um [**ponteiro IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) A **expressão de reinterpretação \_** de cast contorna o sistema de tipos C++, portanto, o compilador não capturará esse erro. No melhor caso, se o objeto não implementar a interface solicitada, a chamada simplesmente falhará. Na pior das hipóteses, a função é bem-sucedida e você tem um ponteiro incompatibilidade. Em outras palavras, o tipo de ponteiro não corresponderá à vtable real na memória. Como você pode imaginar, nada de bom pode acontecer nesse momento.

> [!Note]  
> Uma *vtable* (tabela de método virtual) é uma tabela de ponteiros de função. A vtable é como o COM vincula uma chamada de método à sua implementação em tempo de execução. Não coincidentemente, as vtables são como a maioria dos compiladores C++ implementa métodos virtuais.

 

A [**macro \_ \_ ARGS do IID PPV**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ajuda a evitar essa classe de erro. Para usar essa macro, substitua o seguinte código:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



por este:


```C++
IID_PPV_ARGS(&pFileOpen)
```



A macro insere `__uuidof(IFileOpenDialog)` automaticamente para o identificador de interface, portanto, é garantido que ele corresponderá ao tipo de ponteiro. Este é o código modificado (e correto) :


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Você pode usar a mesma macro com [**QueryInterface:**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>O padrão SafeRelease

A contagem de referência é uma dessas coisas na programação que é basicamente fácil, mas também é entediante, o que facilita o erro. Os erros típicos incluem:

-   Falha ao liberar um ponteiro de interface quando você terminar de usá-lo. Essa classe de bug fará com que seu programa vaze memória e outros recursos, pois os objetos não são destruídos.
-   Chamando [**Versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) com um ponteiro inválido. Por exemplo, esse erro poderá ocorrer se o objeto nunca tiver sido criado. Essa categoria de bug provavelmente fará com que seu programa falha.
-   Desreferenciando um ponteiro de interface após [**a versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) ser chamada. Esse bug pode causar falha no programa. Pior, isso pode fazer com que seu programa falha em um horário aleatório posteriormente, dificultando o controle do erro original.

Uma maneira de evitar esses bugs é chamar [**a Versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) por meio de uma função que libera o ponteiro com segurança. O código a seguir mostra uma função que faz isso:


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



Essa função aceita um ponteiro de interface COM como um parâmetro e faz o seguinte:

1.  Verifica se o ponteiro é **NULL.**
2.  Chamará [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se o ponteiro não for **NULL.**
3.  Define o ponteiro como **NULL.**

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



Se [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) for bem-sucedido, a chamada para `SafeRelease` liberará o ponteiro. Se **CoCreateInstance falhar,** *pFileOpen permanecerá* **NULL.** A `SafeRelease` função verifica isso e ignora a chamada para [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

Também é seguro chamar mais `SafeRelease` de uma vez no mesmo ponteiro, conforme mostrado aqui:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Ponteiros inteligentes COM

A `SafeRelease` função é útil, mas exige que você se lembre de duas coisas:

-   Inicialize cada ponteiro de interface para **NULL.**
-   Chame `SafeRelease` antes que cada ponteiro saia do escopo.

Como programador do C++, você provavelmente está pensando que não deve se lembrar de nenhuma dessas coisas. É por isso que o C++ tem construtores e destruidores. Seria bom ter uma classe que envolve o ponteiro de interface subjacente e inicializa e libera automaticamente o ponteiro. Em outras palavras, queremos algo assim:


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



A definição de classe mostrada aqui está incompleta e não pode ser usável, conforme mostrado. No mínimo, você precisaria definir um construtor de cópia, um operador de atribuição e uma maneira de acessar o ponteiro COM subjacente. Felizmente, você não precisa fazer nada desse trabalho, porque Microsoft Visual Studio fornece uma classe de ponteiro inteligente como parte do Active Template Library (ATL).

A classe de ponteiro inteligente da ATL é denominada **CComPtr**. (Também há uma **classe CComQIPtr,** que não é discutida aqui.) Aqui está o [exemplo abrir caixa de diálogo](example--the-open-dialog-box.md) reescrito para usar **CComPtr**.


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



A principal diferença entre esse código e o exemplo original é que essa versão não chama [**explicitamente**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)Release . Quando a **instância CComPtr** sai do escopo, o destruidor chama **Release** no ponteiro subjacente.

**CComPtr é** um modelo de classe. O argumento de modelo é o tipo de interface COM. Internamente, **o CComPtr** mantém um ponteiro desse tipo. **CComPtr** substitui **operator->()** e **operator&()** para que a classe atue como o ponteiro subjacente. Por exemplo, o código a seguir é equivalente a chamar o **método IFileOpenDialog::Show** diretamente:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** também define um método **CComPtr::CoCreateInstance,** que chama a função [**COM CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com alguns valores de parâmetro padrão. O único parâmetro necessário é o identificador de classe, como mostra o exemplo a seguir:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



O **método CComPtr::CoCreateInstance** é fornecido puramente como uma conveniência; você ainda pode chamar a função [**COM CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) se preferir.

## <a name="next"></a>Avançar

[Tratamento de erro em COM](error-handling-in-com.md)

 

 