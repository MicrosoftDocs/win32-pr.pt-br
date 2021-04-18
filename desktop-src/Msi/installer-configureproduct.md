---
description: O método ConfigureProduct do objeto do instalador instala ou desinstala um produto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configmétodo ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749792"
---
# <a name="installerconfigureproduct-method"></a>Installer.Configmétodo ureProduct

O método **ConfigureProduct** do objeto do [**instalador**](installer-object.md) instala ou desinstala um produto.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o código do produto do produto.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Especifica a configuração de instalação padrão do produto. O parâmetro InstallLevel será ignorado e todos os recursos serão instalados se o parâmetro InstallState for definido como qualquer outro valor que msiInstallStateDefault.

Esse parâmetro deve ser 0 (instalar usando níveis de recurso criados), 65535 (instalar todos os recursos) ou um valor entre 0 e 65535 para instalar um subconjunto de recursos disponíveis.

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

## <a name="remarks"></a>Comentários

O método **ConfigureProduct** exibe a interface do usuário usando as configurações atuais. As configurações de interface do usuário podem ser alteradas modificando a [**Propriedade UILevel (objeto do instalador)**](installer-uilevel.md) antes de chamar o método **ConfigureProduct** .

Se o parâmetro *InstallState* for definido como qualquer outro valor diferente de msiInstallStateDefault, o parâmetro *InstallLevel* será ignorado e todos os recursos do produto serão instalados. Use o método [**ConfigureFeature**](installer-configurefeature.md) para controlar a instalação de recursos individuais quando o parâmetro *InstallState* não estiver definido como msiInstallStateDefault.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Funções de instalação e configuração](installer-function-reference.md)
</dt> </dl>

 

 




