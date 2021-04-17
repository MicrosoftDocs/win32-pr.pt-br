---
description: O método InstallProduct do objeto do instalador abre um pacote do instalador e Inicializa uma sessão de instalação.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Método Installer. InstallProduct
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
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749791"
---
# <a name="installerinstallproduct-method"></a>Método Installer. InstallProduct

O método **InstallProduct** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador e Inicializa uma sessão de instalação.

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

*propertyValues* 
</dt> <dd>

Cadeia de caracteres opcional que contém os pares de propriedade = valor separados por espaço em branco.

Para executar uma instalação administrativa, inclua ACTION = ADMIN em *PropertyValues*. Para obter mais informações, consulte a propriedade [**Action**](action.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para remover completamente um produto, defina REMOVE = ALL em *PropertyValues*. Para obter mais informações, consulte [**remover**](remove.md) propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




