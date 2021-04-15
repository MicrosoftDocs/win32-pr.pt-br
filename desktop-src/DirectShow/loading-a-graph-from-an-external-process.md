---
description: Carregando um grafo a partir de um processo externo
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Carregando um grafo a partir de um processo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570489"
---
# <a name="loading-a-graph-from-an-external-process"></a>Carregando um grafo a partir de um processo externo

GraphEdit pode carregar um grafo de filtro criado por um processo externo. Com esse recurso, você pode ver exatamente qual grafo de filtro seu aplicativo cria, com apenas uma quantidade mínima de código adicional em seu aplicativo.

> [!Note]  
> Esse recurso requer o Windows 2000, o Windows XP ou posterior.

 

> [!Note]  
> A partir do Windows Vista, você deve registrar proppage.dll para habilitar esse recurso. Proppage.dll está incluído no SDK do Windows.

 

O aplicativo deve registrar a instância do grafo de filtro na corrompidos (tabela de objetos em execução). O corrompidos é uma tabela de pesquisa globalmente acessível que controla a execução de objetos. Os objetos são registrados no corrompidos por moniker. Para se conectar ao grafo, o GraphEdit pesquisa o corrompidos em busca de monikers cujo nome de exibição corresponde a um determinado formato:


```C++
!FilterGraph X pid Y
```



em que *X* é o endereço hexadecimal do Gerenciador de gráfico de filtro, e *Y* é a ID do processo, também em hexadecimal.

Quando o aplicativo criar primeiro o grafo de filtro, chame a seguinte função:


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Essa função cria um moniker e uma nova entrada corrompidos para o grafo de filtro. O primeiro parâmetro é um ponteiro para o grafo de filtro. O segundo parâmetro recebe um valor que identifica a nova entrada corrompidos. Antes que o aplicativo libere o gráfico de filtro, chame a função a seguir para remover a entrada corrompidos. O parâmetro *pdwRegister* é o identificador retornado pela função AddToRot.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



O exemplo de código a seguir mostra como chamar essas funções. Neste exemplo, o código que adiciona e remove entradas corrompidos é compilado condicionalmente, para que ela seja incluída somente em compilações de depuração.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Para exibir o gráfico de filtro no GraphEdit, execute o aplicativo e GraphEdit ao mesmo tempo. No menu **arquivo** GraphEdit, clique em **conectar ao grafo remoto...** Na caixa de diálogo **conectar ao grafo** , selecione a ID do processo (PID) do seu aplicativo e clique em **OK**. GraphEdit carrega o gráfico de filtro e o exibe. Não use nenhum outro recurso do GraphEdit nesse grafo — isso pode causar resultados inesperados. Por exemplo, não adicione ou remova filtros, ou pare e inicie o grafo. Feche o GraphEdit antes de sair do aplicativo.

> [!Note]  
> Seu aplicativo pode atingir várias declarações quando ele é encerrado. Você pode ignorá-los.

 

A ilustração a seguir mostra a caixa de diálogo **conectar ao grafo** .

![conectar ao grafo](images/gedit-spy.png)

Quando o GraphEdit carrega o grafo, ele é executado no contexto do aplicativo de destino. Portanto, GraphEdit pode bloquear porque está aguardando o thread. Por exemplo, isso pode ocorrer se você estiver percorrendo o código no depurador.

Esse recurso deve ser usado somente em compilações de depuração do seu aplicativo, não compilações de varejo, pois permite que outros aplicativos exibam ou controlem o grafo de filtro.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Conectando-se a um grafo remoto na linha de comando

O GraphEdit dá suporte a uma opção de linha de comando para carregar automaticamente um grafo remoto na inicialização. A sintaxe do é:


```C++
GraphEdt -a moniker
```



em que *moniker* é um moniker criado usando a função AddToRot, descrito anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Simulando a criação de gráficos com o GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



