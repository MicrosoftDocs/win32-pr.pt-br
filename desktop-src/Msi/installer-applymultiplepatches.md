---
description: O método ApplyMultiplePatches aplica um ou mais patches aos produtos qualificados para receber o patch. O método define a propriedade PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Método Installer. ApplyMultiplePatches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633203"
---
# <a name="installerapplymultiplepatches-method"></a>Método Installer. ApplyMultiplePatches

O método **ApplyMultiplePatches** aplica um ou mais patches aos produtos qualificados para receber o patch. O método define a propriedade [**patch**](patch.md) .

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos caminhos para arquivos de patch. por exemplo: "" c: \\ sus \\ download \\ cache \\ Office \\ sp1. msp; c: \\ sus \\ download \\ cache \\ Office \\ QFE1. msp; c: \\ sus \\ download \\ cache \\ Office \\ QFEn. msp ""

</dd> <dt>

*Product* 
</dt> <dd>

Esse parâmetro fornece o [**ProductCode**](productcode.md) do produto que está sendo corrigido. Esse parâmetro é opcional. Quando esse parâmetro é nulo, os patches são aplicados a todos os produtos qualificados para receber esses patches.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que especifica as configurações de propriedade de linha de comando. Esse parâmetro é opcional. Consulte [sobre propriedades](about-properties.md) e [definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md). Essas propriedades são compartilhadas por todos os produtos de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**DISTRIBUÍDO**](patch.md)
</dt> <dt>

[Definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




