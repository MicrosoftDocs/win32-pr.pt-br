---
description: Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa estar associado a um endereço local.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Associação a um endereço local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771355"
---
# <a name="binding-to-a-local-address"></a>Associação a um endereço local

Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa estar associado a um endereço local. Isso pode ser feito explicitamente chamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))ou implicitamente por [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se o soquete estiver desassociado quando essa função for chamada.

 

 
