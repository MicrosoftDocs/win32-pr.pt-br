---
description: O método InstallProduct do objeto Installer abre um pacote do instalador e inicializa uma sessão de instalação.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Método Installer.InstallProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1605fc0f2e955d6f0364159779ae90f8f59e9ace0f3ff14a1106f7623ab7d99d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630388"
---
# <a name="installerinstallproduct-method"></a>Método Installer.InstallProduct

O **método InstallProduct** do [**objeto Installer**](installer-object.md) abre um pacote do instalador e inicializa uma sessão de instalação.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Cadeia de caracteres necessária que contém o caminho para o pacote de instalação.

</dd> <dt>

*Propertyvalues* 
</dt> <dd>

Cadeia de caracteres opcional que contém pares property=value separados por espaço em branco.

Para executar uma instalação administrativa, inclua ACTION=ADMIN em *propertyValues.* Para obter mais informações, consulte a [**propriedade ACTION.**](action.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para remover completamente um produto, de conjunto REMOVE=ALL em *propertyValues*. Para obter mais informações, consulte [**a propriedade REMOVE.**](remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




