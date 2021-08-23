---
title: Verificando o registro
description: Verificando o registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501646"
---
# <a name="checking-registration"></a>Verificando o registro

Sempre que um aplicativo é carregado, ele deve verificar seu registro para determinar o seguinte:

-   Se as CLSIDs estão presentes no Registro. Se eles não estão presentes, o aplicativo deve se registrar como a configuração original.
-   Se as CLSIDs do aplicativo estão presentes no registro, mas não têm informações relacionadas ao OLE 2. Se esse for o caso, o aplicativo deverá se registrar como a configuração original.
-   Se o caminho que contém entradas de servidor ([LocalServer](localserver.md) e [LocalServer32,](localserver32.md) [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) aponta para o local em que o aplicativo está instalado no momento. Se o caminho não for, reescreva as entradas de caminho para apontar para o local atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 




