---
description: Fornece métodos de enumeração de padrão COM para a interface IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interface IEnumPStoreTypes (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748908"
---
# <a name="ienumpstoretypes-interface"></a>Interface IEnumPStoreTypes

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membros

A interface **IEnumPStoreTypes** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreTypes** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPStoreTypes** tem esses métodos.



| Método                                  | Descrição                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienumpstoretypes-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumpstoretypes-next.md)   | Obtém o próximo tipo de provedor especificado na sequência de enumeração.<br/>                      |
| [**Redefinir**](ienumpstoretypes-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumpstoretypes-skip.md)   | Ignora o tipo de provedor especificado na sequência de enumeração.<br/>                          |



 

## <a name="remarks"></a>Comentários

O objeto enumerador deve ser liberado quando não estiver mais sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
