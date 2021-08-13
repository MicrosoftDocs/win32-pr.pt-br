---
description: O método AddSource do objeto Installer adiciona uma origem à lista de fontes de rede válidas na lista de origem.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Método Installer.AddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c5e2b87a1fc9a660ae835d9fb1cfa465673bb6698144a9695cbfb264535a948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633159"
---
# <a name="installeraddsource-method"></a>Método Installer.AddSource

O **método AddSource** do [**objeto Installer**](installer-object.md) adiciona uma origem à lista de fontes de rede válidas na lista de origem.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o código do produto.

</dd> <dt>

*Usuário* 
</dt> <dd>

Nome de usuário para instalação por usuário; cadeia de caracteres nula ou vazia para instalação por computador.

</dd> <dt>

*Origem* 
</dt> <dd>

Ponteiro para a cadeia de caracteres que especifica a origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




