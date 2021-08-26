---
description: A propriedade Context retorna o contexto deste produto.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Propriedade Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21fb23a595b1f479f2468f0006cca7cd9218de03fc2cc76b794caae79ea45a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129116"
---
# <a name="productcontext-property"></a>Propriedade Product. Context

A propriedade **Context** retorna o contexto deste produto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa propriedade pode retornar um dos valores a seguir.



| Contexto                        | Valor | Significado                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERmanaged | 1     | Produtos sob contexto gerenciado.   |
| \_usuário MSIINSTALLCONTEXT        | 2     | Produtos sob contexto não gerenciado. |
| \_máquina MSIINSTALLCONTEXT     | 4     | Produtos sob o contexto do computador.   |



 

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

 

 




