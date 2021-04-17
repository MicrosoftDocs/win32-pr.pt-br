---
description: A propriedade State retorna o estado de instalação dessa instância do produto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propriedade Product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751185"
---
# <a name="productstate-property"></a>Propriedade Product. State

A propriedade **State** retorna o estado de instalação dessa instância do produto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa propriedade retorna um dos valores a seguir.



| Estado da instalação       | Significado                                |
|--------------------------|----------------------------------------|
| padrão INSTALLstate \_    | Instância do produto instalada localmente. |
| INSTALLstate \_ anunciado | Instância do produto anunciada.        |
| INSTALLstate \_ desconhecido    | Instância do produto desconhecida.           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




