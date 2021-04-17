---
description: Retorna um objeto Recordlist que enumera a lista de produtos.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Propriedade Installer. ProductsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748154"
---
# <a name="installerproductsex-property"></a>Propriedade Installer. ProductsEx

A propriedade **ProductsEx** retorna um objeto [**recordlist**](recordlist-object.md) que enumera a lista de produtos. Essa propriedade chama [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Produto**](product-object.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




