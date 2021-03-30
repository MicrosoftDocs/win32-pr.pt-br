---
title: Verificando registro
description: Verificando registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916087"
---
# <a name="checking-registration"></a>Verificando registro

Cada vez que um aplicativo é carregado, ele deve verificar seu registro para determinar o seguinte:

-   Se os CLSIDs estão presentes no registro. Se eles não estiverem presentes, o aplicativo deverá ser registrado como a configuração original.
-   Se os CLSIDs do aplicativo estão presentes no registro, mas não têm informações relacionadas a OLE 2. Se esse for o caso, o aplicativo deverá ser registrado como a configuração original.
-   Se o caminho que contém entradas de servidor ([LocalServer](localserver.md) e [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) aponta para o local em que o aplicativo está instalado no momento. Se o caminho não tiver, regrave as entradas de caminho para apontar para o local atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 




