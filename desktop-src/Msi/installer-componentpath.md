---
description: A propriedade ComponentPath é uma propriedade somente leitura que retorna o caminho completo para um componente instalado. Se o caminho da chave para o componente for uma chave do Registro, a chave do Registro será retornada.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Propriedade Installer.ComponentPath
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
ms.openlocfilehash: 88601dc4c65d0d3f69a5386ed62d1523c9fa21723e73b1ad4d208d0eff437658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632613"
---
# <a name="installercomponentpath-property"></a>Propriedade Installer.ComponentPath

A **propriedade ComponentPath** é uma propriedade somente leitura que retorna o caminho completo para um componente instalado. Se o caminho da chave para o componente for uma chave do Registro, a chave do Registro será retornada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se o componente for uma chave do Registro, as raízes do Registro serão representadas numericamente. Por exemplo, um caminho do Registro de "HKEY CURRENT USER SOFTWARE Microsoft" seria retornado como \_ \_ \\ \\ "01: \\ SOFTWARE \\ Microsoft". As raízes do Registro retornadas são definidas da seguinte forma:



| Root                    | Valor retornado |
|-------------------------|----------------|
| RAIZ DE \_ CLASSES HKEY \_     | 00             |
| USUÁRIO ATUAL DO HKEY \_ \_     | 01             |
| COMPUTADOR LOCAL HKEY \_ \_    | 02             |
| USUÁRIOS \_ DO HKEY             | 03             |
| HKEY \_ PERFORMANCE \_ DATA | 04             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




