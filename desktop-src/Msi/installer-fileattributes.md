---
description: A propriedade FileAttributes do objeto Installer retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Propriedade Installer.FileAttributes (Windows.storage.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fe43028d856ca26b1c5e8fa21a88a3b77381670ccc044a79f10d3b922f38c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630909"
---
# <a name="installerfileattributes-property"></a>Propriedade Installer.FileAttributes

A **propriedade FileAttributes** do objeto [**Installer**](installer-object.md) retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valor da propriedade

O caminho necessário para o arquivo ou pasta. Um caminho parcial assume o diretório atual.

## <a name="remarks"></a>Comentários

A **propriedade FileAttributes** retorna os valores a seguir.



| Atributo de arquivo              | Valor      | Valor |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| ATRIBUTO \_ DE \_ ARQUIVO TEMPORÁRIO  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2.048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Retornará –1 se o arquivo ou a pasta não existir ou não estiver acessível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| Cabeçalho<br/>  | <dl> <dt>Windows.storage.h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




