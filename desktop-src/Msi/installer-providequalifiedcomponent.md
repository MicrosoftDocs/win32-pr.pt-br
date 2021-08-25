---
description: O método ProvideQualifiedComponent do objeto do instalador retorna o caminho completo do componente e executa qualquer instalação necessária. Se necessário, esse método solicita a origem e incrementa a contagem de uso para o recurso.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Método Installer. ProvideQualifiedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 534f0d29fed41a495c3432ff757d7e269c6b2a5d63c9bfabebe614849f3ab9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828866"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Método Installer. ProvideQualifiedComponent

O método **ProvideQualifiedComponent** do objeto do [**instalador**](installer-object.md) retorna o caminho completo do componente e executa qualquer instalação necessária. Se necessário, esse método solicita a origem e incrementa a contagem de uso para o recurso.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Categoria* 
</dt> <dd>

Especifica a ID do componente solicitado. Esse pode não ser o GUID do próprio componente, mas sim um servidor que fornece a funcionalidade correta, como na coluna ComponentID da [tabela PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Qualificador* 
</dt> <dd>

Especifica um qualificador em uma lista de componentes de propaganda (da [tabela PublishComponent](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Define o modo de instalação. Esse parâmetro pode ser um dos valores mostrados na tabela a seguir.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Fornece o componente, executando qualquer instalação necessária.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                            | Fornece o componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia. Esse modo verifica a existência do arquivo de chave do componente.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                                | Fornece o componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia. Esse modo verifica apenas se o componente está registrado, mas não verifica a existência do arquivo de chave do componente.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                    | Fornece o caminho do componente somente se o recurso existir com um parâmetro InstallState de *msiInstallStateLocal*. Isso verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinação dos sinalizadores msiReinstallMode**</dt> <dt></dt> </dl> | Chama [**ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para o parâmetro *REINSTALLMODE* e, em seguida, fornece o componente.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




