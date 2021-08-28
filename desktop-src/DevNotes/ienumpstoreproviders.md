---
description: Interface IEnumPStoreProviders – fornece métodos de enumeração de padrão COM para a interface IPStore.
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
ms.openlocfilehash: eb73345dd594f3583b4a6cfbc6e0462848d85de0e9470e6bc8177574a2fff20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017704"
---
# <a name="ienumpstoreproviders-interface"></a>Interface IEnumPStoreProviders

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membros

A interface **IEnumPStoreProviders** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPStoreProviders** tem esses métodos.



| Método                                      | Descrição                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreproviders-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumpstoreproviders-next.md)   | Obtém o próximo provedor especificado na sequência de enumeração.<br/>                           |
| [**Definido**](ienumpstoreproviders-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumpstoreproviders-skip.md)   | Ignora o provedor especificado na sequência de enumeração.<br/>                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
