---
title: Suporte para USB 3.0
description: Suporte para USB 3.0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca18cd9f38b17dfaa029738497cf93a43fd85477c9d3c5b30e83f506d5596e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671615"
---
# <a name="support-for-usb-30"></a>Suporte para USB 3.0

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

No Windows 8 e Windows Server 2012, adicionamos suporte para USB 3.0. Fizemos isso adicionando uma nova pilha de software para ligar o controlador de host USB 3.0, chamado de XHC (Controlador de Host eXtensible). Mantemos a paridade da interface, o nível IRQL, o contexto do chamador, o status do erro, a frequência de nova tentativa e assim por diante. Não deve haver nenhuma diferença para você ao interagir com um dispositivo conectado via USB 2.0 versus USB 3.0.

No entanto, se você estiver escrevendo um driver para um novo dispositivo USB 3.0, opte definitivamente por novos recursos USB 3.0.

## <a name="manifestation"></a>Manifestação

As transferências de dispositivo são mais rápidas e menos energia é consumida de um computador por dispositivos USB em geral. Há um risco de que os dispositivos USB existentes não funcionem corretamente quando conectados a uma porta USB 3.0. Isso não deve acontecer e não é esperado, mas, como o software que alimenta USB 3.0 é novo, é um risco.

 

 




