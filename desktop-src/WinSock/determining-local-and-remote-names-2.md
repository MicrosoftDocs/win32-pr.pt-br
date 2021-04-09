---
description: WSPGetSockName é usado para recuperar o endereço local para soquetes associados.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinando nomes locais e remotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010492"
---
# <a name="determining-local-and-remote-names"></a>Determinando nomes locais e remotos

[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) é usado para recuperar o endereço local para soquetes associados. Isso é especialmente útil quando uma chamada [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) foi feita sem fazer um [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) primeiro; **WSPGetSockName** fornece o único meio para determinar a associação local que foi definida implicitamente pelo provedor.

Depois que uma conexão tiver sido configurada, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) poderá ser usado para determinar o endereço do ponto ao qual um soquete está conectado.

 

 
