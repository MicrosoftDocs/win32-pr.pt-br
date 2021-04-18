---
description: O método ConfigureFeature do objeto do instalador configura o estado instalado de um recurso do produto.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configmétodo ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751650"
---
# <a name="installerconfigurefeature-method"></a>Installer.Configmétodo ureFeature

O método **ConfigureFeature** do objeto do [**instalador**](installer-object.md) configura o estado instalado de um recurso do produto.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
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

Especifica a ID do recurso a ser configurado.

</dd> <dt>

*InstallState* 
</dt> <dd>

Especifica o estado de instalação para o recurso. Esse parâmetro deve ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                        | Significado                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | O recurso é anunciado<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | O recurso é instalado localmente.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | O recurso é desinstalado.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | O recurso é instalado para ser executado da origem.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | O recurso é instalado em seu local padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[Funções de instalação e configuração](installer-function-reference.md)
</dt> </dl>

 

 




