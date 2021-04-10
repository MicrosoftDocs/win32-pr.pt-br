---
title: Serviceparameters
description: Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM valor de registro serviceparameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292230"
---
# <a name="serviceparameters"></a>Serviceparameters

Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** . Essa cadeia de caracteres é passada para o serviço como um argumento de linha de comando à medida que ele é iniciado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> </dl>

 

 




