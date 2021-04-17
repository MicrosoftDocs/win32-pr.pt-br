---
description: A propriedade Products é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário e a máquina atuais.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Propriedade Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749585"
---
# <a name="installerproducts-property"></a>Propriedade Installer. Products

A propriedade **Products** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário e a máquina atuais.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para enumerar os produtos, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os produtos não são ordenados, qualquer produto novo tem um índice arbitrário. Isso significa que a função pode retornar produtos em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




