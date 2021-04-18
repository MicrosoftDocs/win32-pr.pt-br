---
description: O esquema para o relatório de erros difere entre as interfaces SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Relatório de erros e validação de parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789344"
---
# <a name="error-reporting-and-parameter-validation"></a>Relatório de erros e validação de parâmetros

O esquema para o relatório de erros difere entre as interfaces SPI e API. Os provedores de serviço do Windows Sockets relatam erros junto com a função retornando, em oposição à abordagem baseada em thread utilizada na API. O \_32.dll Ws2 usa o código de erro por função do provedor de serviços para atualizar o valor de erro por thread obtido por meio da função de API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Os provedores de serviço ainda são necessários, no entanto, para manter o erro baseado em soquete que pode ser recuperado por meio da opção de soquete de erro de SO \_ .

O \_32.dll Ws2 executa a validação de parâmetro somente em chamadas de função que são implementadas inteiramente em si. Os provedores de serviço são responsáveis por executar todas as suas próprias validações de parâmetro.

 

 



