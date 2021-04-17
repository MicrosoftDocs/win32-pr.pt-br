---
description: Para simplificar a implementação do driver o máximo possível, o WIA (aquisição de imagem do Windows) fornece uma biblioteca de serviço minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Biblioteca de serviço minidriver WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813297"
---
# <a name="wia-minidriver-service-library"></a>Biblioteca de serviço minidriver WIA

Para simplificar a implementação do driver o máximo possível, o WIA (aquisição de imagem do Windows) fornece uma biblioteca de serviço minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA. A biblioteca de serviços fornece funções auxiliares para manter a árvore do dispositivo de objetos da [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .

As funções básicas da biblioteca de serviços executam funções auxiliares que a maioria dos drivers de dispositivo precisariam implementar. Essas funções lêem e gravam Propriedades. Eles também criam objetos de item de driver e copiam Propriedades de informações de dispositivo.

 

 



