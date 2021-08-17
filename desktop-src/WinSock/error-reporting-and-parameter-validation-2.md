---
description: O esquema para o relatório de erros difere entre as interfaces SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Relatório de erros e validação de parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132609"
---
# <a name="error-reporting-and-parameter-validation"></a>Relatório de erros e validação de parâmetros

O esquema para o relatório de erros difere entre as interfaces SPI e API. Windows Os provedores de serviço de soquetes relatam erros junto com a função retornando, em oposição à abordagem baseada em thread utilizada na API. O \_32.dll Ws2 usa o código de erro por função do provedor de serviços para atualizar o valor de erro por thread obtido por meio da função de API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Os provedores de serviço ainda são necessários, no entanto, para manter o erro baseado em soquete que pode ser recuperado por meio da opção de soquete de erro de SO \_ .

O \_32.dll Ws2 executa a validação de parâmetro somente em chamadas de função que são implementadas inteiramente em si. Os provedores de serviço são responsáveis por executar todas as suas próprias validações de parâmetro.

 

 



