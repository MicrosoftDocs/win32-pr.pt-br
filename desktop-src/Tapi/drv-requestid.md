---
description: O \_ tipo de dados drv REQUESTID é usado para fornecer um identificador exclusivo para uma solicitação ao provedor de serviços.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788068"
---
# <a name="drv_requestid"></a>DRV \_ REQUESTID

O tipo de dados **drv \_ REQUESTID** é usado para fornecer um identificador exclusivo para uma solicitação ao provedor de serviços. Um valor desse tipo é passado como um parâmetro para cada função que permite a operação assíncrona. Se a operação for assíncrona, o provedor de serviços retornará esse valor como o valor de retorno da função. Sempre que o provedor de serviços sinaliza uma solicitação como assíncrona dessa forma, ele deve eventualmente relatar que a operação foi concluída chamando a função de retorno de chamada [*\_ proc de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) .

A TAPI garante que os valores **drv \_ REQUESTID** fornecidos sejam estritamente positivos, ou seja, entre os valores de 0x00000001 e 0x7FFFFFFF, inclusive. Além disso, os valores são exclusivos, pois nenhum valor retornado de uma função para sinalizar a solicitação como assíncrona será reutilizado antes que a operação seja relatada como concluída.

 

 
