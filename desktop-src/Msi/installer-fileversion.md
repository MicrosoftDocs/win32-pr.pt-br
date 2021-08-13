---
description: O método FileVersion do objeto Installer retorna a cadeia de caracteres de versão ou a cadeia de caracteres de idioma do caminho especificado em Caminho usando o formato no qual o instalador espera encontrá-los no banco de dados.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Método Installer.FileVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 492ebb0c7678b7819f3abc423517dcf77d071b81009c3b12017b1b627bb84057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630578"
---
# <a name="installerfileversion-method"></a>Método Installer.FileVersion

O **método FileVersion** do objeto [**Installer**](installer-object.md) retorna a cadeia de caracteres de versão ou a cadeia de caracteres de idioma do caminho especificado em *Caminho* usando o formato no qual o instalador espera encontrá-los no banco de dados. Para versões, essa é uma cadeia de caracteres no formato " \# . . . " \# \# \# . Para idioma, essa é a ID da linguagem decimal.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* 
</dt> <dd>

Cadeia de caracteres necessária que contém o caminho para o arquivo.

</dd> <dt>

*Idioma* 
</dt> <dd>

Sinalizador para designar se o valor retornado é uma ID de idioma ou uma cadeia de caracteres de versão. TRUE retorna o idioma, FALSE retorna a versão. Esse parâmetro é opcional, com um valor padrão false.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




