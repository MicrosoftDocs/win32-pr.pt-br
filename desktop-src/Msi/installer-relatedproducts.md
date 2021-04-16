---
description: A propriedade RelatedProducts somente leitura retorna um objeto StringList que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário atual e computador com uma propriedade UpgradeCode especificada em sua tabela de propriedades.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Propriedade Installer. RelatedProducts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749996"
---
# <a name="installerrelatedproducts-property"></a>Propriedade Installer. RelatedProducts

A propriedade **RelatedProducts** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário atual e computador com uma propriedade [**UpgradeCode**](upgradecode.md) especificada em sua [tabela de propriedades](property-table.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valor da propriedade

O código de atualização de produtos relacionados que o instalador enumera.

## <a name="remarks"></a>Comentários

Para enumerar os produtos relacionados, um aplicativo é iterado por meio da [**StringList**](stringlist-object.md) usando uma construção for each. Como os produtos relacionados não são ordenados, qualquer produto relacionado novo tem um índice arbitrário. Isso significa que a função pode retornar produtos relacionados em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




