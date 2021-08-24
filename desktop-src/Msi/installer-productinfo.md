---
description: A propriedade ProductInfo é uma propriedade somente leitura que retorna o valor do atributo especificado para um produto instalado ou publicado.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Propriedade Installer. ProductInfo (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745286"
---
# <a name="installerproductinfo-property"></a>Propriedade Installer. ProductInfo

A propriedade **ProductInfo** é uma propriedade somente leitura que retorna o valor do atributo especificado para um produto instalado ou publicado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

A propriedade **ProductInfo** ("LocalPackage") não retorna necessariamente um caminho para o pacote armazenado em cache. As instalações do modo de manutenção não devem ser invocadas do LocalPackage. O pacote armazenado em cache é apenas para usos internos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP.<br/> |
| Cabeçalho<br/>  | <dl> <dt>Oemupgex. h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




