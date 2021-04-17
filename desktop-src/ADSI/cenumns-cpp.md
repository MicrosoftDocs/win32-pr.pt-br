---
title: CENUMNS. CPP
description: No componente de provedor de exemplo, a enumeração de um objeto de namespace usa os métodos, de cenumns. cpp, listados na tabela a seguir.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105749123"
---
# <a name="cenumnscpp"></a>CENUMNS. CPP

No componente de provedor de exemplo, a enumeração de um objeto de namespace usa os métodos, de cenumns. cpp, listados na tabela a seguir.



| Método                                              | Descrição                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum:: criar**                  | Crie um objeto para permitir a enumeração de um objeto de namespace do ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Construtor padrão.                                                                                                                                     |
| **CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum** | Destruidor padrão.                                                                                                                                      |
| **CSampleDSNamespaceEnum:: Next**                    | Recupera o número especificado de elementos do objeto namespace indicado.                                                                            |
| **CSampleDSNamespaceEnum::EnumObjects**             | Gerenciar a recuperação de ponteiros de interface para os objetos.                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Busque o conjunto de ponteiros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Busque o próximo objeto. Se for encontrado, crie um objeto Active Directory genérico e recupere seu ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |



 

 

 