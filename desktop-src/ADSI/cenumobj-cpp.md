---
title: CENUMOBJ. CPP
description: No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj. cpp, listadas na tabela a seguir.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641823"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. CPP

No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj. cpp, listadas na tabela a seguir.



| Método                                                 | Descrição                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum:: criar**                     | Crie um objeto para habilitar a enumeração de objetos Active Directory genéricos.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inicialização.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gerenciar a recuperação de objetos.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recupere o conjunto de ponteiros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que correspondem ao filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recuperar um objeto e fazer a correspondência com o filtro. Se corresponder, empacote-o em objeto genérico e retorne um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gerenciar a recuperação de objetos.                                                                                                                                        |
| **CSampleDSGenObjectEnum:: Next**                       | Recupera o número especificado de elementos do objeto de enumeração indicado.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Verifique se a classe de objeto corresponde a uma na lista de filtros.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Gerenciar a matriz de filtros.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Adicione uma nova classe de objeto ao filtro e defina o filtro como contíguo.                                                                                                |
| **FreeFilterList**                                     | Libere o filtro.                                                                                                                                                      |



 

 

 