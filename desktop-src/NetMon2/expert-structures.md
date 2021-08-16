---
description: As funções auxiliares de especialistas fornecidas por Monitor de Rede e funções auxiliares comuns usam as estruturas descritas na tabela a seguir.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Estruturas de especialistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939013"
---
# <a name="expert-structures"></a>Estruturas de especialistas

As funções auxiliares de especialistas fornecidas por Monitor de Rede e funções auxiliares comuns usam as estruturas descritas na tabela a seguir.



| Estrutura                                              | Description                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Associa uma DLL de especialista à sua configuração.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Fornece dados de configuração brutos.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Fornece informações sobre a DLL de especialista. Monitor de Rede usa as informações.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Fornece informações sobre um quadro.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Fornece informações de inicialização sobre o especialista.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Fornece o status atual de um especialista em execução.                                                       |
| [**FILTERobject**](filterobject.md)                   | Define as características do filtro de exibição para um especialista.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Fornece informações sobre uma linha exibida no Visualizador de especialistas.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Fornece informações que definem uma coluna na Visualizador de Eventos.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Fornece um contêiner para todos os dados possíveis inseridos em uma coluna em uma linha na Visualizador de Eventos.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | O ponto de entrada na variante que indica qual elemento da União deve ser usado e como formatá-lo. |



 

Monitor de Rede também fornece funções de exportação (funções auxiliares que o especialista pode chamar) e enumerações.



| Para obter informações sobre                                          | Consulte                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportar funções que fornecem pontos de entrada para sua DLL de especialista. | [Funções de exportação de DLL de especialista](expert-dll-export-functions.md)               |
| Funções auxiliares que podem ser chamadas por especialistas e analisadores.    | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |
| Funções auxiliares que são chamadas apenas por especialistas.              | [Funções de especialista](expert-functions.md)                                     |
| Enumerações usadas por estruturas e funções de especialistas.          | [Enumerações de especialistas](expert-enumerations.md)                               |



 

 

 



