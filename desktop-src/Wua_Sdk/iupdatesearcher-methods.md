---
description: A interface IUpdateSearcher define os métodos a seguir.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Métodos IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769263"
---
# <a name="iupdatesearcher-methods"></a>Métodos IUpdateSearcher

A interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define os métodos a seguir.



| Método                                                              | Descrição                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | Inicia a execução de uma pesquisa assíncrona para atualizações. A pesquisa usa as opções de pesquisa que estão configuradas no momento. |
| [**Endsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | Conclui uma pesquisa assíncrona de atualizações.                                                                             |
| [**EscapeString**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | Converte uma cadeia de caracteres em uma cadeia de caracteres que pode ser usada como um valor literal em uma cadeia de caracteres de critérios de pesquisa.                          |
| [**GetTotalHistoryCount**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | Retorna o número de eventos de atualização no computador.                                                                      |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | Consulta de forma síncrona o computador para o histórico de eventos de atualização.                                                      |
| [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | Executa uma pesquisa síncrona para atualizações. A pesquisa usa as opções de pesquisa que estão configuradas no momento.              |



 

 

 



