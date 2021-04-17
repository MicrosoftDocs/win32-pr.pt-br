---
description: O método FileVersion do objeto instalador retorna a cadeia de caracteres da versão ou a cadeia de caracteres do caminho especificado em path usando o formato no qual o instalador espera encontrá-las no banco de dados.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Método Installer. FileVersion
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
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747971"
---
# <a name="installerfileversion-method"></a>Método Installer. FileVersion

O método **FileVersion** do objeto [**instalador**](installer-object.md) retorna a cadeia de caracteres da versão ou a cadeia de caracteres do caminho especificado em *Path* usando o formato no qual o instalador espera encontrá-las no banco de dados. Para versões, esta é uma cadeia de caracteres \# no \# formato ".. \# . \# ". Para o idioma, essa é a ID de idioma decimal.

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

Sinalizador para designar se o valor retornado é uma ID de idioma ou uma cadeia de caracteres de versão. TRUE retorna o idioma; FALSE retorna a versão. Esse parâmetro é opcional, com um valor padrão de FALSE.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




