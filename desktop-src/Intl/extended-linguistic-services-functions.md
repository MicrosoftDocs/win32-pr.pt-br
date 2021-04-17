---
description: O ELS dá suporte às funções definidas na tabela a seguir.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funções de serviços linguísticas estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747358"
---
# <a name="extended-linguistic-services-functions"></a>Funções de serviços linguísticas estendidos

O ELS dá suporte às funções definidas na tabela a seguir.



| Função                                                 | Descrição                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Uma função de retorno de chamada definida pelo aplicativo que processa de forma assíncrona os dados produzidos pela função **MappingRecognizeText** .                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Faz com que um serviço ELS execute uma ação após a ocorrência do reconhecimento de texto.                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Libera memória e recursos alocados durante uma operação de reconhecimento de texto ELS.                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Libera memória e recursos alocados para o aplicativo interagir com um ou mais serviços ELSs.                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Recupera uma lista de serviços disponíveis com suporte da plataforma ELS, juntamente com informações associadas, de acordo com os critérios especificados pelo aplicativo. |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Chamadas em um serviço ELS para reconhecer texto.                                                                                                   |



 

 

 



