---
description: A propriedade ComponentQualifiers é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de qualificadores registrados para o componente especificado.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Propriedade Installer. ComponentQualifiers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752852"
---
# <a name="installercomponentqualifiers-property"></a>Propriedade Installer. ComponentQualifiers

A propriedade **ComponentQualifiers** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de qualificadores registrados para o componente especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Valor da propriedade

Um GUID de cadeia de caracteres que representa a categoria do [componente](publishcomponent-table.md).

## <a name="remarks"></a>Comentários

Para enumerar qualificadores, o aplicativo itera por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os qualificadores não são ordenados, qualquer qualificador novo tem um índice arbitrário, o que significa que a função pode retornar qualificadores em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




