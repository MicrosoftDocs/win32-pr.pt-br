---
title: Como usar OLE em controles de edição Rich
description: Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d825a9876005cadb20e4fc7717f766582ab12224f4f86995319357875d24230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311676"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Como usar OLE em controles de edição Rich

Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-interface"></a>Usar uma interface de edição rica

Os controles de edição avançados expõem algumas de suas funcionalidades por meio de interfaces de Component Object Model (COM). Ao obter uma interface de um controle, você obtém a capacidade de trabalhar com outros objetos dentro do controle. Você pode obter essa interface enviando a mensagem [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) . Na interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) , você pode obter interfaces usadas no [modelo de objeto de texto](text-object-model.md).

Outra interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), é implementada por aplicativos para definir o comportamento do controle quando ele interage com objetos.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Inserir um objeto em um controle de edição rico

O exemplo de código a seguir insere um objeto File em um controle rich edit. se um programa estiver associado ao tipo de arquivo na máquina do usuário (por exemplo, Microsoft Excel para um arquivo de .xls), o conteúdo do arquivo será exibido no controle; caso contrário, um ícone será exibido.

1.  Obtenha a interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Crie um armazenamento estruturado.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Configure o formato de dados.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Obtenha um ponteiro para o site de exibição.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Crie o objeto e recupere sua interface **IUnknown** .

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  Obtenha a interface IOleObject para o objeto.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Para garantir que as referências sejam contadas corretamente, notifique o objeto que ele está contido.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Configurar informações do objeto.

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  Mover o cursor para o fim do texto e adicionar um retorno de carro.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Insira o objeto.

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Limpar.

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Usando IRichEditOleCallback

Os aplicativos implementam a interface [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) para responder a consultas ou ações relacionadas a OLE que são executadas por um controle de edição rico. Você associa a implementação da interface ao controle enviando uma mensagem em [**\_ SETOLECALLBACK**](em-setolecallback.md) . O controle então chama métodos em sua implementação da interface, conforme apropriado.

Por exemplo, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) é chamado quando o usuário tenta arrastar ou colar um objeto no controle. Se seu aplicativo puder aceitar os dados, sua implementação do método retornará S \_ OK; caso contrário, ele retornará um código de erro. O método também pode executar alguma outra ação, como aviso o usuário de que os arquivos desse tipo não podem ser colocados no controle.

## <a name="complete-insertobject-example-function"></a>Função de exemplo InsertObject completa

O exemplo de código a seguir demonstra os trechos de código anteriores combinados em uma função completa que inclui o tratamento de erros.


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




