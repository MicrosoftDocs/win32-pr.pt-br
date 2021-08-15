---
description: Fornece os métodos de enumeração COM padrão para a interface IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interface IEnumPStoreItems (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f5952dbaff2560ae4c2fc59af73246c2cd5c1d050bb53bc3c7b9091c8a39822f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542236"
---
# <a name="ienumpstoreitems-interface"></a>Interface IEnumPStoreItems

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornece os métodos de enumeração COM padrão para a interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membros

A interface **IEnumPStoreItems** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreItems** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPStoreItems** tem esses métodos.



| Método                                  | Descrição                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreitems-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumpstoreitems-next.md)   | Obtém o próximo item de dados especificado na sequência de enumeração.<br/>                          |
| [**Definido**](ienumpstoreitems-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumpstoreitems-skip.md)   | Ignora o item de dados especificado na sequência de enumeração.<br/>                              |



 

## <a name="remarks"></a>Comentários

É necessário liberar cada item depois de enumera-lo. O objeto Enumerator também deve ser liberado quando não estiver mais sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
