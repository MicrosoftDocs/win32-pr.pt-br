---
description: O método ClearSourceList do objeto Installer remove todas as fontes de rede da lista de origem.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Método Installer.ClearSourceList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16cc37556d217a217b814b5ce87cb705cd3105d4a8c2ad3f503d617aeda2cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633034"
---
# <a name="installerclearsourcelist-method"></a>Método Installer.ClearSourceList

O **método ClearSourceList** do [**objeto Installer**](installer-object.md) remove todas as fontes de rede da lista de origem.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ClearSourceList(
  Product,
  User
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

[**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




