---
description: Carregando um arquivo de projeto
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Carregando um arquivo de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163778"
---
# <a name="loading-a-project-file"></a>Carregando um arquivo de projeto

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Para carregar um arquivo de projeto, você precisa de dois componentes: o analisador XML e uma linha do tempo vazia. O analisador XML lê um arquivo de projeto XML e cria cada objeto definido no arquivo. Em seguida, ele insere os objetos na linha do tempo e define os atributos da linha do tempo, como a taxa de quadros padrão. O exemplo de código a seguir carrega um arquivo.


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



O analisador expõe a interface [**IXml2Dex**](ixml2dex.md) , que contém métodos para carregar e salvar arquivos de projeto. A linha do tempo expõe a interface [**IAMTimeline**](iamtimeline.md) , que contém métodos para manipular a linha do tempo e criar novos objetos de linha do tempo. Chame a função **CoCreateInstance** para criar cada componente, conforme mostrado. Lembre-se de que, ao criar uma nova instância, você está incrementando a contagem de referência na interface. Para evitar vazamentos de memória, sempre libere uma interface quando você estiver usando-a. Neste exemplo, o ponteiro para **IXml2Dex** não é necessário para mais nada, para que você possa liberar a interface. O ponteiro para **IAMTimeline** ainda é necessário para visualizar a linha do tempo.

O método [**IXml2Dex:: readxmlfile**](ixml2dex-readxmlfile.md) lê o arquivo especificado e popula a linha do tempo com os objetos definidos no arquivo. O nome do arquivo é especificado usando um valor **BSTR** . Para encurtar o exemplo, o nome do arquivo no exemplo é fornecido como uma cadeia de caracteres literal. Normalmente, você o obtém de uma caixa de diálogo de arquivo aberto ou algo semelhante.

Se o método **ReadXml** for bem-sucedido, ele retornará um código de êxito. Caso contrário, ele retornará um código de erro como VFW \_ E \_ formato de \_ arquivo inválido \_ . Sempre verifique o valor de retorno para tratar as condições de erro normalmente. Novamente, para resumir, o código de exemplo não verifica se há erros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Carregando e visualizando um projeto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



