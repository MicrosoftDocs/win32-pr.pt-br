---
description: Fornece métodos de enumeração de padrão COM para a interface IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interface IEnumPStoreProviders (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752322"
---
# <a name="ienumpstoreproviders-interface"></a>Interface IEnumPStoreProviders

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membros

A interface **IEnumPStoreProviders** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPStoreProviders** tem esses métodos.



| Método                                      | Descrição                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienumpstoreproviders-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumpstoreproviders-next.md)   | Obtém o próximo provedor especificado na sequência de enumeração.<br/>                           |
| [**Redefinir**](ienumpstoreproviders-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumpstoreproviders-skip.md)   | Ignora o provedor especificado na sequência de enumeração.<br/>                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
