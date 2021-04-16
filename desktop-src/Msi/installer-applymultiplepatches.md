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
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750003"
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

Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos caminhos para arquivos de patch. Por exemplo: "" c: \\ SUS \\ download de \\ cache \\ Office \\ SP1. msp; c: \\ SUS \\ baixar o \\ cache \\ Office \\ QFE1. msp; c: \\ SUS \\ Download \\ cache \\ Office \\ QFEn. msp ""

</dd> <dt>

*Product* 
</dt> <dd>

Esse parâmetro fornece o [**ProductCode**](productcode.md) do produto que está sendo corrigido. Esse parâmetro é opcional. Quando esse parâmetro é nulo, os patches são aplicados a todos os produtos qualificados para receber esses patches.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que especifica as configurações de propriedade de linha de comando. Esse parâmetro é opcional. Consulte [sobre propriedades](about-properties.md) e [definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md). Essas propriedades são compartilhadas por todos os produtos de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.<br/> |
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

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




