---
description: para simplificar a implementação do driver o máximo possível, a aquisição de imagem Windows (WIA) fornece uma biblioteca de serviço Minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Biblioteca de serviço minidriver WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0008e19fbbdb31000535fa10f34bfacebfd6c6180964fa3e3fb18502f22a28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207926"
---
# <a name="wia-minidriver-service-library"></a>Biblioteca de serviço minidriver WIA

para simplificar a implementação do driver o máximo possível, a aquisição de imagem Windows (WIA) fornece uma biblioteca de serviço Minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA. A biblioteca de serviços fornece funções auxiliares para manter a árvore do dispositivo de objetos da [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .

As funções básicas da biblioteca de serviços executam funções auxiliares que a maioria dos drivers de dispositivo precisariam implementar. Essas funções lêem e gravam Propriedades. Eles também criam objetos de item de driver e copiam Propriedades de informações de dispositivo.

 

 



