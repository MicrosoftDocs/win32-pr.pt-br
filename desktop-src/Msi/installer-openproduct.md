---
description: O método OpenProduct do objeto do instalador abre um pacote do instalador para um produto instalado usando o código do produto e retorna um objeto de sessão.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Método Installer. OpenProduct
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
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752848"
---
# <a name="installeropenproduct-method"></a>Método Installer. OpenProduct

O método **OpenProduct** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador para um produto instalado usando o código do produto e retorna um objeto de [**sessão**](session-object.md) .

## <a name="syntax"></a>Sintaxe


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*productCode* 
</dt> <dd>

Cadeia de caracteres necessária que contém o código de produto exclusivo (um [GUID](guid.md)) ou um descritor de ativação escrito pelo instalador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Observe que apenas um objeto de [**sessão**](session-object.md) pode ser aberto por um único processo. **OpenProduct** não pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




