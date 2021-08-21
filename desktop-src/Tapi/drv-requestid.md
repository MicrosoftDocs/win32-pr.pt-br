---
description: O tipo de \_ dados REQUESTID DRV é usado para fornecer um identificador exclusivo para uma solicitação para o provedor de serviços.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e75e593ccbf2d9d8135fbb52762a83a539dc29f8ef9446735d0898d3437e37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866536"
---
# <a name="drv_requestid"></a>DRV \_ REQUESTID

O **tipo de dados \_ REQUESTID DRV** é usado para fornecer um identificador exclusivo para uma solicitação para o provedor de serviços. Um valor desse tipo é passado como um parâmetro para cada função que permite uma operação assíncrona. Se a operação for assíncrona, o provedor de serviços retornará esse valor como o valor de retorno da função. Sempre que o provedor de serviços sinaliza uma solicitação como assíncrona dessa maneira, ele deve relatar que a operação é concluída chamando a função de retorno de chamada [*Proc \_*](/windows/win32/api/tspi/nc-tspi-async_completion) de conclusão.

A TAPI garante que os valores **\_ DE REQUESTID** do DRV que ele fornece sejam estritamente positivos, ou seja, entre os valores de 0x00000001 e 0x7FFFFFFF, inclusive. Além disso, os valores são exclusivos, pois nenhum valor retornado de uma função para sinalizar a solicitação como assíncrona será reatribuir antes que a operação seja relatada como concluída.

 

 
