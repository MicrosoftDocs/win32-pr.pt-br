---
description: Para cada produto listado pelo pacote de patches como qualificado para receber o patch, o método ApplyPatch do objeto do instalador invoca uma instalação e define a propriedade PATCH para o caminho do pacote de patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Método Installer. ApplyPatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c4bcb1ba1dc988f3c28188b4b448dba611b83c6cffbe7f942710569ac089776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633222"
---
# <a name="installerapplypatch-method"></a>Método Installer. ApplyPatch

Para cada produto listado pelo pacote de patches como qualificado para receber o patch, o método **ApplyPatch** do objeto do [**instalador**](installer-object.md) invoca uma instalação e define a propriedade [**patch**](patch.md) para o caminho do pacote de patch.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PatchPackage* 
</dt> <dd>

Especifica um caminho para o pacote de patch.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Se *InstallType* for definido como MsiInstallTypeNetworkImage, *InstallPackage* especificará o caminho para o produto a ser corrigido. Se *InstallType* for definido como MsiInstallTypeDefault e *InstallPackage* for definido como 0, o instalador aplicará o patch a todos os produtos qualificados listados no pacote de patch.

Se *InstallType* for msiInstallTypeSingleInstance, o instalador aplicará o patch ao produto especificado por *InstallPackage*. Nesse caso, outros produtos qualificados listados no pacote de patch são ignorados e o parâmetro *InstallPackage* contém a cadeia de caracteres terminada em nulo que representa o código do produto da instância a ser corrigida. esse tipo de instalação requer a versão Windows Installer fornecida com o Windows Server 2003 ou posterior ou Windows Installer XP SP1 ou posterior.

</dd> <dt>

*InstallType* 
</dt> <dd>

Esse parâmetro especifica o tipo de instalação a ser corrigido. O parâmetro *InstallType* será ignorado se *InstallPackage* for omitido.



| Valor                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indica uma instalação administrativa. Nesse caso, *InstallPackage* deve ser definido como um caminho de pacote. Um valor de 1 para msiInstallTypeNetworkImage especifica uma instalação administrativa.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Pesquisa o sistema para obter os produtos a serem corrigidos. Nesse caso, *InstallPackage* deve ser uma cadeia de caracteres vazia.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Aplicar patch ao produto especificado por *InstallPackage*. *InstallPackage* é o código do produto da instância a ser corrigida. esse tipo de instalação requer a versão Windows Installer fornecida com o Windows Server 2003 ou posterior ou Windows Installer XP SP1 ou posterior. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Especifica as configurações de propriedade que estão sendo definidas na linha de comando. Consulte a seção Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Como o delimitador de lista para transformações, origens e patches é um ponto e vírgula, esse caractere não deve ser usado para nomes de arquivo ou caminhos.

A propriedade [**REINSTALL**](reinstall.md) é necessária ao aplicar uma [atualização pequena](small-updates.md) ou um patch de [atualização secundária](minor-upgrades.md) . Sem essa propriedade, o patch é registrado no sistema, mas não pode atualizar arquivos.

**Windows Installer 2,0:** Você deve definir a propriedade [**REINSTALL**](reinstall.md) na linha de comando ao aplicar uma [atualização pequena](small-updates.md) ou um patch de [atualização secundária](minor-upgrades.md) . Para patches que não usam um [tipo de ação personalizada 51](custom-action-type-51.md) para definir automaticamente as propriedades **reinstalar** e [**reinstalarmode**](reinstallmode.md) , a propriedade **reinstalar** deve ser explicitamente definida com o parâmetro *CommandLine* . Defina a propriedade **REINSTALL** para listar os recursos afetados pelo patch ou use uma configuração padrão prática de "REINSTALL = ALL". O valor padrão da propriedade **REinstallmode** é "omus".

**Windows Installer 3,0 e posterior:** a partir do Windows Installer versão 3,0, a propriedade [**reinstall**](reinstall.md) é configurada pelo instalador e não precisa ser definida na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




