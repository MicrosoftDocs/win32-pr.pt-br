---
title: Suporte para USB 3,0
description: Suporte para USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641964"
---
# <a name="support-for-usb-30"></a>Suporte para USB 3,0

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

No Windows 8 e no Windows Server 2012, adicionamos suporte para USB 3,0. Fizemos isso adicionando uma nova pilha de software para ligar o controlador de host USB 3,0, chamado de XHC (controlador de host extensível). Mantivemos a paridade da interface, o nível de IRQL, o contexto do chamador, o status do erro, a frequência de repetição e assim por diante. Não deve haver nenhuma diferença para você ao interagir com um dispositivo conectado por USB 2,0 versus USB 3,0.

No entanto, se você estiver escrevendo um driver para um novo dispositivo USB 3,0, definitivamente, opte por novos recursos de USB 3,0.

## <a name="manifestation"></a>Manifestação

As transferências de dispositivo são mais rápidas e menos energia são consumidas de um PC por dispositivos USB em geral. Há um risco de que os dispositivos USB existentes não funcionem corretamente quando conectados a uma porta USB 3,0. Isso não deve acontecer e não é esperado, mas, como o software que alimenta o USB 3,0 é novo, é um risco.

 

 




