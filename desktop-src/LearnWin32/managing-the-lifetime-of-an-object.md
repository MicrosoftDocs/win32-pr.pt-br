---
title: Gerenciando o tempo de vida de um objeto
description: Saiba como gerenciar os métodos AddRef e Release para controlar o tempo de vida de um objeto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566145"
---
# <a name="managing-the-lifetime-of-an-object"></a>Gerenciando o tempo de vida de um objeto

Há uma regra para interfaces COM que ainda não mencionamos. Cada interface COM deve herdar, direta ou indiretamente, de uma interface chamada [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Essa interface fornece alguns recursos de linha de base para os quais todos os objetos COM devem dar suporte.

A interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) define três métodos:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

O método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permite que um programa consulte os recursos do objeto em tempo de execução. Vamos falar mais sobre isso no próximo tópico, [solicitando um objeto para uma interface](asking-an-object-for-an-interface.md). Os métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) são usados para controlar o tempo de vida de um objeto. Este é o assunto deste tópico.

## <a name="reference-counting"></a>Contagem de referência

Independentemente do que mais um programa possa fazer, em algum momento ele alocará e liberará recursos. A alocação de um recurso é fácil. Saber quando liberar o recurso é difícil, especialmente se o tempo de vida do recurso se estender além do escopo atual. Esse problema não é exclusivo do COM. Qualquer programa que aloca memória de heap deve resolver o mesmo problema. Por exemplo, o C++ usa destruidores automáticos, enquanto C# e Java usam coleta de lixo. COM usa uma abordagem chamada *contagem de referência*.

Cada objeto COM mantém uma contagem interna. Isso é conhecido como a contagem de referência. A contagem de referência acompanha Quantas referências ao objeto estão ativas no momento. Quando o número de referências cai para zero, o objeto se exclui. A última parte vale a pena repetir: o objeto se exclui. O programa nunca exclui explicitamente o objeto.

Aqui estão as regras para a contagem de referência:

-   Quando o objeto é criado pela primeira vez, sua contagem de referência é 1. Neste ponto, o programa tem um único ponteiro para o objeto.
-   O programa pode criar uma nova referência duplicando (copiando) o ponteiro. Ao copiar o ponteiro, você deve chamar o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) do objeto. Esse método incrementa a contagem de referência em uma.
-   Quando você terminar de usar um ponteiro para o objeto, deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). O método **Release** decrementa a contagem de referência em uma. Ele também invalida o ponteiro. Não use o ponteiro novamente depois de chamar a **versão**. (Se você tiver outros ponteiros para o mesmo objeto, poderá continuar a usar esses ponteiros.)
-   Quando você tiver chamado [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) com cada ponteiro, a contagem de referência de objeto do objeto chegará a zero e o objeto se excluirá.

O diagrama a seguir mostra um caso simples, mas típico.

![Diagrama que mostra um caso simples de contagem de referência.](images/com04.png)

O programa cria um objeto e armazena um ponteiro (*p*) para o objeto. Neste ponto, a contagem de referência é 1. Quando o programa for concluído usando o ponteiro, ele chamará [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). A contagem de referência é diminuída para zero e o objeto se exclui. Agora, *p* é inválido. É um erro usar *p* para qualquer chamada de método adicional.

O próximo diagrama mostra um exemplo mais complexo.

![ilustração que mostra a contagem de referência](images/com05.png)

Aqui, o programa cria um objeto e armazena o ponteiro *p*, como antes. Em seguida, o programa copia *p* para uma nova variável, *p*. Neste ponto, o programa deve chamar [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para incrementar a contagem de referência. A contagem de referência agora é 2, e há dois ponteiros válidos para o objeto. Agora suponha que o programa termine de usar *p*. O programa chama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), a contagem de referência vai para 1 e *p* não é mais válida. No entanto, *p* ainda é válido. Posteriormente, o programa terminará de usar *q*. Portanto, ele chama **Release** novamente. A contagem de referência vai para zero e o objeto se exclui.

Você deve estar imaginando por que o programa copiaria *p*. Há dois motivos principais: primeiro, você pode desejar armazenar o ponteiro em uma estrutura de dados, como uma lista. Em segundo lugar, talvez você queira manter o ponteiro além do escopo atual da variável original. Portanto, você o copiaria para uma nova variável com um escopo maior.

Uma vantagem da contagem de referência é que você pode compartilhar ponteiros entre diferentes seções de código, sem os vários caminhos de código que coordenam para excluir o objeto. Em vez disso, cada caminho de código simplesmente chama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando o caminho do código é feito usando o objeto. O objeto lida com a exclusão no horário correto.

## <a name="example"></a>Exemplo

Aqui está o código do [exemplo da caixa de diálogo abrir](example--the-open-dialog-box.md) novamente.

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

A contagem de referência ocorre em dois locais neste código. Primeiro, se o programa criar com êxito o objeto de caixa de diálogo de item comum, ele deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pFileOpen* .

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

Em segundo lugar, quando o método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) retorna um ponteiro para a interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , o programa deve chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pItem* .

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Observe que em ambos os casos, a chamada de [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) é a última coisa que acontece antes que o ponteiro saia do escopo. Observe também que a **versão** é chamada somente depois de testar o **HRESULT** para obter êxito. Por exemplo, se a chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) falhar, o ponteiro *pFileOpen* não será válido. Portanto, seria um erro para chamar **Release** no ponteiro.

## <a name="next"></a>Avançar

[Solicitando um objeto para uma interface](asking-an-object-for-an-interface.md)