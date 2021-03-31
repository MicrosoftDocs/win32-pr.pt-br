---
title: O manipulador padrão e os manipuladores personalizados
description: O manipulador padrão e os manipuladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916095"
---
# <a name="the-default-handler-and-custom-handlers"></a>O manipulador padrão e os manipuladores personalizados

O manipulador padrão, uma implementação fornecida pelo OLE, é usado pela maioria dos aplicativos como o manipulador. Um aplicativo implementa um manipulador personalizado quando os recursos do manipulador padrão são insuficientes. Um manipulador personalizado pode substituir completamente o manipulador padrão ou usar partes da funcionalidade que ele fornece quando apropriado. No último caso, o manipulador de aplicativos é implementado como um objeto de agregação composto por um novo objeto de controle e o manipulador padrão. Os manipuladores de aplicativo/padrão de combinação também são conhecidos como *manipuladores em processo*. O *manipulador de comunicação remota* é usado para objetos que não são atribuídos a um CLSID no registro do sistema ou que não têm nenhum manipulador especificado. Tudo o que é necessário a partir de um manipulador para esses tipos de objetos é que eles passam informações entre o limite do processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipuladores de objetos](object-handlers.md)
</dt> </dl>

 

 




