---
description: A propriedade MediaDisks enumera todos os discos de mídia para esta instância do produto. Essa propriedade chama o MsiSourceListEnumMediaDisks. Retorna as informações de disco como uma matriz de objetos Record.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Propriedade Product.MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 00496739c9e51b5a735bf57788cdc47be0c41e177201ef445f58ea3748fb062f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042196"
---
# <a name="productmediadisks-property"></a>Propriedade Product.MediaDisks

A **propriedade MediaDisks** enumera todos os discos de mídia para esta instância do produto. Essa propriedade chama [**o MsiSourceListEnumMediaDisks.**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) Retorna as informações de disco como uma matriz de [**objetos Record.**](record-object.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Em cada registro, o primeiro campo contém a ID do disco, o segundo campo contém o rótulo do volume e o terceiro campo contém o prompt de disco registrado para o disco.

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

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




