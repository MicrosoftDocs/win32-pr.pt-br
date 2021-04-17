---
description: O método UseFeature do objeto do instalador incrementa a contagem de uso de um recurso específico e retorna o estado de instalação para esse recurso. Esse método deve ser usado para indicar a intenção de um aplicativo usar um recurso.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Método Installer. UseFeature
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
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747965"
---
# <a name="installerusefeature-method"></a>Método Installer. UseFeature

O método **UseFeature** do objeto do [**instalador**](installer-object.md) incrementa a contagem de uso de um recurso específico e retorna o estado de instalação para esse recurso. Esse método deve ser usado para indicar a intenção de um aplicativo usar um recurso.

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

Especifica o código do produto do produto.

</dd> <dt>

*Recurso* 
</dt> <dd>

Identifica o recurso a ser usado.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Esse parâmetro deve ser *msiInstallModeNoDetection*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **UseFeature** só deve ser usado em recursos conhecidos para publicação. O aplicativo deve determinar o status do recurso chamando a propriedade [**featurestate**](installer-featurestate.md) ou os [**recursos**](installer-features.md) ou seus equivalentes de API.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




