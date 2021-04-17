---
description: A classe CMSPThread implementa o thread de trabalho do MSPs.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754199"
---
# <a name="cmspthread"></a>CMSPThread

A classe **CMSPThread** implementa o thread de trabalho do MSP. As classes base usam esse thread de trabalho para várias finalidades. Um mecanismo de item de trabalho leve e genérico é fornecido para permitir que o MSP derivado Use esse thread para seus próprios itens de trabalho síncronos ou assíncronos, o que for possível. O thread também bombas mensagens e dá suporte ao tratamento de APCs (embora APCs não sejam usados nas classes base).

Quando vários endereços like estão presentes (ou seja, quando a mesma implementação de MSP da mesma DLL é instanciada várias vezes), a classe thread garante a escalabilidade usando automaticamente um único thread para todos os endereços. A interface para a classe thread é tal que a implementação MSP pode pensar na classe thread como um thread privado e não precisa se preocupar com os outros endereços que podem estar compartilhando.

Definido em MSPthrd. h.

 

 



