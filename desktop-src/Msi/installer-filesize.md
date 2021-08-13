---
description: O método FileSize do objeto Installer usa chamadas à API win32 para retornar o tamanho do arquivo especificado em Path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Método Installer.FileSize
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
ms.openlocfilehash: f585da776d348e7c774d4671a230881f2ec0e4ddaca8a63842d59a9b77a61972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630685"
---
# <a name="installerfilesize-method"></a>Método Installer.FileSize

O **método FileSize** do [**objeto Installer**](installer-object.md) usa chamadas à API do Win32 para retornar o tamanho do arquivo especificado no *Caminho*.

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




