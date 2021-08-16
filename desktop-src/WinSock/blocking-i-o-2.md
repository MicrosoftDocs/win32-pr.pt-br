---
description: A forma mais simples de E/S no Windows Sockets 2 está bloqueando a E/S.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Bloqueando entrada/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c65991f4401a5069718fb39172a9d59db4536a83ab4e2f99948d7c300eb4042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322610"
---
# <a name="blocking-inputoutput"></a>Bloqueando entrada/saída

A forma mais simples de E/S no Windows Sockets 2 está bloqueando a E/S. Conforme mencionado em [Modos e Sinalizadores de](socket-attribute-flags-and-modes-2.md)Atributo de Soquete, os soquetes são criados no modo de bloqueio por padrão. Qualquer operação de E/S com um soquete de bloqueio não retornará até que a operação tenha sido totalmente concluída. Portanto, qualquer thread só pode executar uma operação de E/S por vez. Por exemplo, se um thread emite uma operação de recebimento e nenhum dado está disponível no momento, o thread será bloqueado até que os dados se torne disponíveis e seja colocado no buffer do thread. Embora isso seja simples, não é necessariamente a maneira mais eficiente de fazer E/S (consulte [Pseudo Blocking e True Blocking](pseudo-vs--true-blocking-2.md) para obter mais informações).

 

 



