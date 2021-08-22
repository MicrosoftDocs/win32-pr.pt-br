---
title: Criar e executar exemplo de StoClien
description: O StoClien trabalha em cooperação com um objeto de copapel em um servidor COM para obter armazenamento persistente de desenhos em arquivos compostos COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Criar e executar exemplo de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3d9526e81fc3fb2d6a0cfb03e8943ccf68688096588122da87861d8c88e531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663456"
---
# <a name="create-and-run-stoclien-sample"></a>Criar e executar exemplo de StoClien

O **StoClien** trabalha em cooperação com um objeto de copapel em um servidor com para obter armazenamento persistente de desenhos em arquivos compostos com. Para obter mais informações sobre o uso de fluxos do copaper no arquivo composto fornecido para o copaper por **StoClien**, consulte o exemplo de [**StoServe**](structured-storage-server-sample--stoserve-.md) e STOSERVE.HTM. A construção de copapel e sua interface IPaper também são abordadas no exemplo de **StoServe** .

## <a name="code-tour"></a>Tour pelo código

Os principais tópicos abordados neste Tour de código são:

-   Como o **CGuiPaper** encapsula o comportamento de GUI do papel de desenho eletrônico do **StoClien**
-   Como o **StoClien** captura e exibe a atividade de desenho interativa
-   Como o objeto **CGuiPaper** usa o copapel para gravar dados de desenho
-   Como uma conexão IPaperSink é usada na repintura
-   Como os métodos **Load** e **Save** do CPapFile usam o armazenamento estruturado em arquivos compostos

Como a classe **CGuiBall** usada nos exemplos FRECLIEN e CONCLIEN encapsulava o comportamento de uma bola de saltação, **StoClien** usa uma classe **CGuiPaper** do C++ para encapsular os dados e o comportamento da GUI do papel de desenho eletrônico.

A tabela a seguir lista os arquivos pertinentes ao exemplo de **StoClien** .



| Arquivos        | Descrição                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Breve descrição da amostra.                                                                                                        |
| MAKEFILE     | O makefile genérico para criar o exemplo de código.                                                                               |
| STOCLIEN. T   | O arquivo de inclusão para o aplicativo **StoClien** . Contém declarações de classe, protótipos de função e identificadores de recurso.   |
| STOCLIEN. CPP | O arquivo de implementação principal para STOCLIEN.EXE. Tem a implementação WinMain e CMainWindow, bem como a expedição do menu principal. |
| STOCLIEN. RC  | O arquivo de definição de recurso do aplicativo.                                                                                        |
| STOCLIEN. ICO | O recurso de ícone do aplicativo.                                                                                                   |
| STOCLIEN. PAP | Um arquivo de desenho de papel padrão para o aplicativo.                                                                                |
| Pincel. CUR   | Uma imagem de lápis para o cursor da janela do cliente.                                                                                     |
| Coletar. T       | A declaração de classe para a classe de objeto COPaperSink COM.                                                                      |
| Coletar. CPP     | Arquivo de implementação para a classe de objeto COPaperSink COM.                                                                        |
| PAPFILE. T    | A declaração de classe para a classe **CPapFile** C++.                                                                            |
| PAPFILE. CPP  | Arquivo de implementação para a classe **CPapFile** C++.                                                                              |
| GUIPAPER. T   | A declaração de classe para a classe **CGuiPaper** C++.                                                                           |
| GUIPAPER. CPP | Arquivo de implementação para a classe **CGuiPaper** C++.                                                                             |
| STOCLIEN. DSP | Microsoft Visual Studio Project arquivo.                                                                                            |



 

## <a name="compound-files"></a>arquivos compostos

O **StoClien** se baseia em copapel para gravar dados de desenho. Ele também se baseia em copapel para armazenar os dados em um arquivo composto. No entanto, em uma divisão típica de trabalho entre o cliente COM e o servidor, o **StoClien** compartilha parte da responsabilidade pelo armazenamento de arquivos. Essa divisão de trabalho é importante em aplicativos COM em que o cliente é um contêiner e o servidor é um objeto incorporado. Nesse arranjo, o cliente é responsável por criar ou abrir um arquivo de armazenamento estruturado, enquanto o objeto de servidor é responsável por usar esse armazenamento para suas próprias finalidades de armazenamento de dados. Isso pode envolver o objeto de servidor que cria subarmazenamentos no armazenamento que é fornecido a ele. Em geral, ele envolve o objeto Server criando objetos Stream no armazenamento. O uso de fluxos de armazenamento do copaper é detalhado no exemplo de **StoClien** .

A interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) é usada pelo objeto de cliente e de servidor para executar operações de arquivo. a implementação dos arquivos compostos da arquitetura de Armazenamento estruturada é usada. As funções de serviço padrão são usadas para operações em arquivos compostos. Por exemplo, a função [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) inicialmente cria um arquivo composto e retorna um ponteiro **IStorage** que pode ser usado para manipular o arquivo. Essa função específica é chamada em **StoClien**. A interface **IStorage** obtida é passada como um parâmetro para o copapel para seu uso. O objeto de copapel não cria ou abre arquivos compostos por conta própria: ele usa as interfaces **IStorage** e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para trabalhar em arquivos compostos que são fornecidos a ele.

Essas interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) não são implementadas em **StoClien** ou **StoServe**. Eles são implementados nas bibliotecas COM. Quando um ponteiro para uma dessas interfaces é obtido, seus métodos são essencialmente usados como um conjunto de serviços para operar em um arquivo composto.

 

 




