---
title: REGDSAPI. CPP
description: No componente de provedor de exemplo, as funções que representam uma API que acessa diretamente o sistema operacional nativo estão em Regdsapi. cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291783"
---
# <a name="regdsapicpp"></a>REGDSAPI. CPP

No componente de provedor de exemplo, as funções que representam uma API que acessa diretamente o sistema operacional nativo estão em Regdsapi. cpp. O componente de provedor de exemplo implementa seu serviço de diretório no registro. Para escrever um provedor que acessa seu próprio serviço de diretório, crie suas próprias implementações dessa API. As funções com suporte são listadas na tabela a seguir.



| Método                             | Descrição                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Abra este objeto por nome. Se o parâmetro de tipo de classe de esquema for **nulo**, preencha o tipo encontrado. Recupere um identificador no objeto.                                                             |
| **SampleDSCloseObject**            | Use o identificador recuperado por **SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Recupere o identificador em um objeto enumerador para gerenciar a enumeração de nomes diferenciados relativos (RDNs) de um objeto de contêiner.                                                          |
| **SampleDSNextRDN**                | Usando o identificador recuperado por **SampleDSRDNEnum**, obtenha o próximo nome distinto relativo desse objeto de contêiner.                                                                        |
| **SampleDSFreeEnum**               | Libere o objeto enumerador alocado em **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modifique as propriedades de um objeto no serviço de diretório de acordo com o identificador do objeto e uma lista de atributos e seus valores.                                                              |
| **SampleDSReadObject**             | Leia as propriedades do objeto do serviço de diretório. Mapeie a sintaxe do armazenamento nativo para os valores de sintaxe do ADS apropriados. Manipule Propriedades com vários valores de acordo. |
| **SampleDSGetPropertyDefinition**  | No esquema, pesquise todas as definições de propriedade e seus atributos para esse tipo de objeto de classe de esquema.                                                                                     |
| **SampleDSGetPropertyDefinition**  | No esquema, pesquise essa propriedade e seus atributos por nome.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Memória livre alocada por **GetPropertyDefinition**.                                                                                                                                            |
| **SampleDSGetTypeText**            | Obter o tipo de classe de esquema de um objeto no formato de texto.                                                                                                                                         |
| **SampleDSGetType**                | Obter o tipo de classe de esquema de um objeto.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Dado um identificador no objeto de classe de esquema e um nome de propriedade, recupere as informações de propriedade, como sintaxe e assim por diante.                                                                      |
| **Listas**                       | Libere a memória usada por uma lista de LPWSTR \_ .                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Recupere o conjunto de todas as definições de classe de esquema e seus dados associados do esquema.                                                                                                    |
| **SampleDSGetClassDefinition**     | Recuperar dados sobre uma classe de esquema específica no esquema.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Considerando o nome de uma classe de esquema, pesquise seus dados associados, como propriedades obrigatórias.                                                                                                      |
| **SampleDSAddObject**              | Adicione um objeto no serviço de diretório.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Remova um objeto do serviço de diretório.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Crie um buffer de memória para dados de atributo e dados de operação.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Libere o buffer criado em **SampleDSCreateBuffer**.                                                                                                                                           |



 

 

 




