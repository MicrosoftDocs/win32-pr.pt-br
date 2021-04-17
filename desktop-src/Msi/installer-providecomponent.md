---
description: O método ProvideComponent do objeto do instalador retorna o caminho completo do componente e executa qualquer instalação necessária.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Método Installer. ProvideComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751438"
---
# <a name="installerprovidecomponent-method"></a>Método Installer. ProvideComponent

O método **ProvideComponent** do objeto do [**instalador**](installer-object.md) retorna o caminho completo do componente e executa qualquer instalação necessária. Se necessário, o método **ProvideComponent** do objeto [**instalador**](installer-object.md) solicita a origem e incrementa a contagem de uso para o recurso.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
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

Especifica a ID do recurso que contém o componente.

</dd> <dt>

*Componente* 
</dt> <dd>

Especifica o código do componente.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Define o modo de instalação. Esse parâmetro pode ser um dos valores mostrados na tabela a seguir.



| Nome                                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | Fornece o caminho do componente, executando qualquer instalação, se necessário.<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                           | Fornece o caminho do componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia. Esse modo verifica a existência do arquivo de chave do componente.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                               | Fornece o caminho do componente somente se o recurso existir. Caso contrário, retorna uma cadeia de caracteres vazia. Esse modo verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                   | Fornece o caminho do componente somente se o recurso existir com um parâmetro InstallState de *msiInstallStateLocal*. Isso verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinação dos sinalizadores msiReinstallMode**</dt><dt></dt> </dl> | Chama [**ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para o parâmetro *REINSTALLMODE* e, em seguida, fornece o componente.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **ProvideComponent** combina a funcionalidade de [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)e [**ComponentPath**](installer-componentpath.md). O método **ProvideComponent** simplifica a sequência de chamada, mas também incrementa a contagem de uso e deve ser usado com cautela para evitar contagens de uso imprecisas. O método **ProvideComponent** também fornece menos flexibilidade do que uma série de chamadas individuais para os métodos e propriedades mencionados anteriormente.

Se o aplicativo estiver se recuperando de uma situação inesperada, o aplicativo provavelmente já chamou [**UseFeature**](installer-usefeature.md) e incrementou a contagem de uso. Nesse caso, o aplicativo deve evitar incrementar a contagem de uso chamando o método [**ConfigureFeature**](installer-configurefeature.md) em vez do método **ProvideComponent** .

A opção msiInstallModeExisting não pode ser usada em combinação com sinalizadores msiReinstallMode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




