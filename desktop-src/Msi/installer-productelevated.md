---
description: A propriedade ProductElevated do objeto do instalador retornará true se o produto for gerenciado ou false se o produto não for gerenciado.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Instalador::P Propriedade roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 515964481c62e4588f3d9b75d168bffd2876cb22ce526e8ec0eaa41e226c110e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129386"
---
# <a name="installerproductelevated-property"></a>Instalador::P Propriedade roductElevated

A propriedade **ProductElevated** do objeto do [**instalador**](installer-object.md) retornará true se o produto for gerenciado ou false se o produto não for gerenciado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valor da propriedade

O GUID do código completo do produto. Este parâmetro é necessário.

## <a name="remarks"></a>Comentários

A propriedade **ProductElevated** usa a função [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) . O retorno da propriedade não leva em conta a política [AlwaysInstallElevated](alwaysinstallelevated.md) .

## <a name="examples"></a>Exemplos

O exemplo de script a seguir demonstra o uso da propriedade **ProductElevated** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




