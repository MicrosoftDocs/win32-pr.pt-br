---
title: Consultando dispositivos de áudio auxiliares
description: Consultando dispositivos de áudio auxiliares
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- áudio de onda, consultando dispositivos de áudio auxiliares
- áudio auxiliar, consultando dispositivos
- interface de áudio auxiliar
- dispositivos de áudio auxiliares, consultando
- consultando dispositivos de áudio auxiliares
- áudio auxiliar, interface
- áudio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037566"
---
# <a name="querying-auxiliary-audio-devices"></a>Consultando dispositivos de áudio auxiliares

Nem todos os sistemas de multimídia têm suporte de áudio auxiliar. Você pode usar a função [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) para determinar o número de dispositivos auxiliares controláveis presentes em um sistema.

Para obter informações sobre um dispositivo de áudio auxiliar específico, use a função [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) . Essa função preenche uma estrutura [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) com informações sobre os recursos de um dispositivo especificado. Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo.

 

 