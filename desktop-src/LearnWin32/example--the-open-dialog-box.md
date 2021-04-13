---
title: Exemplo da caixa de diálogo abrir
description: O exemplo de formas que estamos usando é um pouco forçado. Vamos recorrer a um objeto COM que você pode usar em um programa do Windows real na caixa de diálogo abrir.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365979"
---
# <a name="example-the-open-dialog-box"></a>Exemplo: a caixa de diálogo abrir

O `Shapes` exemplo que estamos usando é um pouco forçado. Vamos recorrer a um objeto COM que você pode usar em um programa do Windows real: a caixa de diálogo **abrir** .

![captura de tela mostrando a caixa de diálogo abrir](images/fileopen01.png)

Para mostrar a caixa de diálogo **abrir** , um programa pode usar um objeto com chamado objeto de caixa de diálogo de item comum. A caixa de diálogo item comum implementa uma interface chamada [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), que é declarada no arquivo de cabeçalho ShObjIdl. h.

Aqui está um programa que exibe a caixa de diálogo **abrir** para o usuário. Se o usuário selecionar um arquivo, o programa mostrará uma caixa de diálogo que contém o nome do arquivo.


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



Esse código usa alguns conceitos que serão descritos posteriormente no módulo, portanto, não se preocupe se você não entender tudo aqui. Aqui está uma estrutura de tópicos básica do código:

1.  Chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.
2.  Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o objeto de caixa de diálogo de item comum e obter um ponteiro para a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) do objeto.
3.  Chame o método **show** do objeto, que mostra a caixa de diálogo para o usuário. Esse método é bloqueado até que o usuário desperca a caixa de diálogo.
4.  Chame o método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) do objeto. Esse método retorna um ponteiro para um segundo objeto COM, chamado de objeto de *item de shell* . O item de Shell, que implementa a interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , representa o arquivo selecionado pelo usuário.
5.  Chame o método [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) do item do Shell. Esse método obtém o caminho do arquivo, na forma de uma cadeia de caracteres.
6.  Mostrar uma caixa de mensagem que exibe o caminho do arquivo.
7.  Chame [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) para cancelar a inicialização da biblioteca com.

As etapas 1, 2 e 7 chamam funções que são definidas pela biblioteca COM. Essas são funções COM genéricas. Etapas 3 a 5 métodos de chamada que são definidos pelo objeto de caixa de diálogo de item comum.

Este exemplo mostra as duas variedades de criação de objeto: a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) genérica e um método ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) que é específico para o objeto de caixa de diálogo de item comum.

## <a name="next"></a>Avançar

[Gerenciando o tempo de vida de um objeto](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de caixa de diálogo aberta](open-dialog-box-sample.md)
</dt> </dl>

 

 