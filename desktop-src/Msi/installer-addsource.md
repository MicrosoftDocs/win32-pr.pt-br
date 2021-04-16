---
description: O método addsource do objeto instalador adiciona uma fonte à lista de fontes de rede válidas na SourceList.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Método Installer. addsource
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
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751196"
---
# <a name="installeraddsource-method"></a>Método Installer. addsource

O método **addsource** do objeto [**instalador**](installer-object.md) adiciona uma fonte à lista de fontes de rede válidas na SourceList.

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

Nome de usuário para instalação por usuário; Cadeia de caracteres nula ou vazia para instalação por máquina.

</dd> <dt>

*Origem* 
</dt> <dd>

Ponteiro para a cadeia de caracteres que especifica a origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




