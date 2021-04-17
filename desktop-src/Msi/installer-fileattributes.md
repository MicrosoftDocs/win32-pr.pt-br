---
description: A propriedade FileAttributes do objeto instalador retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Propriedade Installer. FileAttributes (Windows. Storage. h)
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
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751439"
---
# <a name="installerfileattributes-property"></a>Propriedade Installer. FileAttributes

A propriedade **FileAttributes** do objeto [**instalador**](installer-object.md) retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valor da propriedade

O caminho necessário para o arquivo ou a pasta. Um caminho parcial assume o diretório atual.

## <a name="remarks"></a>Comentários

A propriedade **FileAttributes** retorna os valores a seguir.



| Atributo de arquivo              | Valor      | Valor |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| atributo de arquivo \_ \_ temporário  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2.048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Retornará – 1 se o arquivo ou a pasta não existir ou não estiver acessível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| parâmetro<br/>  | <dl> <dt>Windows. Storage. h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




