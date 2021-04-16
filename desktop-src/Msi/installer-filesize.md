---
description: O método FileSize do objeto instalador usa as chamadas à API do Win32 para retornar o tamanho do arquivo especificado em path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Método Installer. FileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747764"
---
# <a name="installerfilesize-method"></a>Método Installer. FileSize

O método **filesize** do objeto [**instalador**](installer-object.md) usa as chamadas à API do Win32 para retornar o tamanho do arquivo especificado em *Path*.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* 
</dt> <dd>

Cadeia de caracteres necessária que contém o caminho para o arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




