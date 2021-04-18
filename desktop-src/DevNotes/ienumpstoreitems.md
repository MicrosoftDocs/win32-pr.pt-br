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
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749286"
---
# <a name="ienumpstoreitems-interface"></a>Interface IEnumPStoreItems

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornece os métodos de enumeração COM padrão para a interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membros

A interface **IEnumPStoreItems** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreItems** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPStoreItems** tem esses métodos.



| Método                                  | Descrição                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienumpstoreitems-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumpstoreitems-next.md)   | Obtém o próximo item de dados especificado na sequência de enumeração.<br/>                          |
| [**Redefinir**](ienumpstoreitems-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumpstoreitems-skip.md)   | Ignora o item de dados especificado na sequência de enumeração.<br/>                              |



 

## <a name="remarks"></a>Comentários

É necessário liberar cada item depois de enumera-lo. O objeto Enumerator também deve ser liberado quando não estiver mais sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
