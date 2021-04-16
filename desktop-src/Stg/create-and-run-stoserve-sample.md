---
title: Criar e executar exemplo de StoServe
description: O exemplo de cliente e outros exemplos relacionados devem ser compilados antes que você possa executar o cliente.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754098"
---
# <a name="create-and-run-stoserve-sample"></a>Criar e executar exemplo de StoServe

O exemplo de cliente e outros exemplos relacionados devem ser compilados antes que você possa executar o cliente. Para obter mais detalhes sobre como criar os exemplos, consulte [como criar exemplos](how-to-build-samples.md). Se você já tiver criado os exemplos apropriados, STOCLIEN.EXE será o executável do cliente a ser executado para o exemplo **StoServe** .

## <a name="code-tour"></a>Tour pelo código

A tabela a seguir lista os arquivos pertinentes ao exemplo de **StoServe** .



| Arquivos        | Descrição                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | Descrição de exemplo breve                                                                                                  |
| MAKEFILE     | O makefile genérico para criar o STOSERVE.DLL exemplo de código desta lição.                                            |
| STOSERVE. T   | O arquivo de inclusão para declarar como importado ou definir como exportado as funções de serviço no STOSERVE.DLL.                 |
| STOSERVE. CPP | O arquivo de implementação principal para STOSERVE.DLL. Tem DllMain e as funções de servidor COM (por exemplo, DllGetClassObject). |
| STOSERVE. PARTICULAR | O arquivo de definição de módulo. Exporta funções de invólucro de servidor.                                                             |
| STOSERVE. RC  | O arquivo de definição de recurso de DLL para o executável.                                                                      |
| STOSERVE. ICO | O recurso de ícone para o executável.                                                                                     |
| Servidor. T     | O arquivo de inclusão do objeto C++ de controle de servidor.                                                                       |
| Servidor. CPP   | O arquivo de implementação do objeto C++ de controle de servidor.                                                                |
| Padrões. T    | O arquivo de inclusão para objetos COM da fábrica de classes do servidor.                                                              |
| Padrões. CPP  | O arquivo de implementação para as fábricas de classe do servidor.                                                                 |
| Connect. T    | O arquivo de inclusão para as classes enumerador de ponto de conexão, ponto de conexão e enumerador de conexão.                |
| Connect. CPP  | O arquivo de implementação para os objetos enumerador de ponto de conexão, ponto de conexão e enumerador de conexão.         |
| Documentos. T      | O arquivo de inclusão para a classe de objeto COM do copaper.                                                                        |
| Documentos. CPP    | O arquivo de implementação para a classe de objeto COM de copapel e os pontos de conexão.                                       |
| STOSERVE. DSP | Microsoft Visual Studio arquivo de projeto.                                                                                     |



 

Os principais tópicos abordados neste Tour de código são:

-   Os métodos de interface [**IPaper**](ipaper-methods.md) .
-   Uso do copaper da interface [**IPaperSink**](ipapersink-methods.md) para notificações do cliente.
-   [**Estruturas**](structures---stoserve.md) em StoServe.
-   [Considerações sobre Unicode](unicode-considerations.md).

 

 




