---
description: A propriedade Sources enumera todas as fontes para a instância do produto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Propriedade Product.Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c54b9563898b093af324b02ca6a5bf48fbddf62b31c22a3d492c1132c46f13f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753916"
---
# <a name="productsources-property"></a>Propriedade Product.Sources

A **propriedade Sources** enumera todas as fontes para a instância do produto. Essa propriedade chama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e retorna a matriz de cadeias de caracteres e aceita o tipo de origem como argumento. O tipo de origem pode ser MSISOURCETYPE \_ NETWORK ou URL MSISOURCETYPE. \_

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Valor da propriedade

O tipo de origem a ser enumerado. O valor pode ser *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct é definido como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Produto**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




