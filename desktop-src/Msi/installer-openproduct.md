---
description: O método OpenProduct do objeto Installer abre um pacote do instalador para um produto instalado usando o código do produto e retorna um objeto Session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Método Installer.OpenProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129376"
---
# <a name="installeropenproduct-method"></a>Método Installer.OpenProduct

O **método OpenProduct** do objeto [**Installer**](installer-object.md) abre um pacote do instalador para um produto instalado usando o código do produto e retorna um [**objeto Session.**](session-object.md)

## <a name="syntax"></a>Sintaxe


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Productcode* 
</dt> <dd>

Cadeia de caracteres necessária que contém o código do produto exclusivo (um [GUID)](guid.md)ou um descritor de ativação escrito pelo instalador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Observe que apenas um [**objeto Session**](session-object.md) pode ser aberto por um único processo. **OpenProduct não** pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




