---
title: CENUMOBJ. Cpp
description: No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj.cpp, listadas na tabela a seguir.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad1e91a58080dc11f7d8da11f3e3fd59dc2ce75431ee2998d8d4e11011bbb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023674"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. Cpp

No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj.cpp, listadas na tabela a seguir.



| Método                                                 | Descrição                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum::Create**                     | Crie um objeto para habilitar a enumeração de objetos genéricos do Active Directory.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inicialização.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gerenciar a recuperação de objetos.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recupere o conjunto de [**ponteiros IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que corresponderem ao filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recuperar um objeto e corresponder ao filtro. Se ele corresponde, wrap-lo em um objeto genérico e retornar um [**ponteiro IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gerencie a recuperação dos objetos.                                                                                                                                        |
| **CSampleDSGenObjectEnum::Next**                       | Recupere o número especificado de elementos do objeto de enumeração indicado.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Verifique se a classe de objeto corresponde a uma na lista de filtros.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Gerencie a matriz de filtros.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Adicione uma nova classe de objeto ao filtro e de definir o filtro como contíguo.                                                                                                |
| **FreeFilterList**                                     | Liberar o filtro.                                                                                                                                                      |



 

 

 