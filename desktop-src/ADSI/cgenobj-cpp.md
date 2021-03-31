---
title: CGENOBJ. CPP
description: No exemplo de componente de provedor, os métodos de objeto Active Directory genéricos, com suporte em cgenobj. cpp, são listados na tabela a seguir.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634891"
---
# <a name="cgenobjcpp"></a>CGENOBJ. CPP

No exemplo de componente de provedor, os métodos de objeto Active Directory genéricos, com suporte em cgenobj. cpp, são listados na tabela a seguir.



| Método                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Construtor padrão.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject:: ~ CSampleDSGenObject**                                             | Destruidor padrão.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject:: creategenéricaobject**                                             | Crie um objeto genérico do ADS. Inicialize conforme apropriado.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Crie esse objeto em seu contêiner pai.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Salve as propriedades deste objeto (Limpe o cache).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Crie um objeto genérico e carregue seus dados de tipo.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject:: QueryInterface**                                                  | Retorne o ponteiro de interface solicitado, se disponível.                                                                                                                                                                                                                                                                       |
| Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) padrão, incluindo implementações para:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (incluindo o mapeamento do tipo de dados nativo para o tipo Variant) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (incluindo o mapeamento de tipo Variant para tipo de dados nativo)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (atualizar o cache de propriedades)<br/> [**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (salvar o cache de propriedades)<br/> |
| Métodos do [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) padrão, incluindo implementações para: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**obter \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**obter \_ filtro**](iadscontainer-property-methods.md)<br/> [**Criar**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Apagar**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Rotina do utilitário.                                                                                                                                                                                                                                                                                                            |



 

 

 





