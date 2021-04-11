---
title: CPRPOBJ. CPP
description: No componente de provedor de exemplo, os métodos de objeto de propriedade, em cprpobj. cpp, são listados na tabela a seguir.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159302"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. CPP

No componente de provedor de exemplo, os métodos de objeto de propriedade, em cprpobj. cpp, são listados na tabela a seguir.



| Método                                                 | Descrição                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Construtor padrão.                                                                                                                          |
| **CSampleDSProperty:: ~ CSampleDSProperty**              | Destruidor padrão.                                                                                                                           |
| **CSampleDSProperty:: CreateProperty**                  | Crie um objeto de propriedade ADS, pesquisando as definições de atributo chamando **SampleDSGetPropertyDefinition**.                              |
| **CSampleDSProperty:: CreateProperty**                  | Dada a definição do atributo, crie um objeto de propriedade, definindo a correspondência entre as sintaxes de anúncios com suporte e as sintaxes do provedor. |
| **CSampleDSProperty::AllocatePropertyObject**          | Crie um objeto de propriedade e carregue seus dados de tipo.                                                                                               |
| **CSampleDSProperty:: QueryInterface**                  | Retorne o ponteiro de interface solicitado, se disponível.                                                                                          |
| Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) padrão.                 |                                                                                                                                                |
| Métodos [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) padrão. |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Defina a correspondência entre a ID da sintaxe e a sintaxe ADS.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Defina a correspondência entre a ID da sintaxe e a sintaxe do provedor.                                                                          |



 

 

 




