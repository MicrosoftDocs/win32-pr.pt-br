---
title: Serviceparameters
description: Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM valor de registro serviceparameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129958"
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

 

 




