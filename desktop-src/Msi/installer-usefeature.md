---
description: O método UseFeature do objeto Installer incrementa a contagem de uso para um recurso específico e retorna o estado de instalação para esse recurso. Esse método deve ser usado para indicar a intenção de um aplicativo de usar um recurso.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Método Installer.UseFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b320ce72271bb7ee90ac85a376b103d868e6f740a2e853daf58bb478dc79ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142150"
---
# <a name="installerusefeature-method"></a>Método Installer.UseFeature

O **método UseFeature** do objeto [**Installer**](installer-object.md) incrementa a contagem de uso para um recurso específico e retorna o estado de instalação para esse recurso. Esse método deve ser usado para indicar a intenção de um aplicativo de usar um recurso.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o código do produto.

</dd> <dt>

*Recurso* 
</dt> <dd>

Identifica o recurso a ser usado.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Esse parâmetro deve ser *msiInstallModeNoDetection.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O **método UseFeature** só deve ser usado em recursos conhecidos por serem publicados. O aplicativo deve determinar o status do recurso chamando a propriedade [**FeatureState**](installer-featurestate.md) ou [**a propriedade Recursos**](installer-features.md) ou seus equivalentes de API.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




