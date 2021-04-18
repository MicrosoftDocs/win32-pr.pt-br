---
description: A propriedade ComponentPath é uma propriedade somente leitura que retorna o caminho completo para um componente instalado. Se o caminho da chave do componente for uma chave do registro, a chave do registro será retornada.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Propriedade Installer. ComponentPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752040"
---
# <a name="installercomponentpath-property"></a>Propriedade Installer. ComponentPath

A propriedade **ComponentPath** é uma propriedade somente leitura que retorna o caminho completo para um componente instalado. Se o caminho da chave do componente for uma chave do registro, a chave do registro será retornada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se o componente for uma chave do registro, as raízes do registro serão representadas numericamente. Por exemplo, um caminho de registro de "HKEY \_ Current \_ user \\ software \\ Microsoft" seria retornado como "01: \\ software \\ Microsoft". As raízes do registro retornadas são definidas da seguinte maneira:



| Root                    | Valor retornado |
|-------------------------|----------------|
| \_raiz de classes hKey \_     | 00             |
| HKEY \_ Current \_ User     | 01             |
| \_máquina local \_ HKEY    | 02             |
| usuários de HKEY \_             | 03             |
| \_dados de desempenho de hKey \_ | 04             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




