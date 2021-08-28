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
ms.openlocfilehash: befa632feae7b4c57983f13a28e695051842cb5d1a2ff0908e6ffd011c6e4918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753946"
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
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




