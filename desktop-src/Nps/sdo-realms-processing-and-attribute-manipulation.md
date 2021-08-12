---
title: Processamento de territórios e manipulação de atributos
description: O processamento de territórios, que também é conhecido como manipulação de atributos, refere-se à transformação do nome do usuário que está solicitando acesso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618942"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Processamento de territórios e manipulação de atributos

> [!Note]  
> o IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

O processamento de territórios, que também é conhecido como manipulação de atributos, refere-se à transformação do nome do usuário que está solicitando acesso. A ID de estação de chamada e a ID de estação chamada também podem ser manipuladas. As regras de processamento de territórios são parte da coleção de atributos do perfil de proxy.

Para cada manipulação, você precisa criar dois atributos [de regra de manipulação](/windows/desktop/Nps/sdo-manipulation-rule) . Cada um desses atributos é um valor de cadeia de caracteres. A primeira regra contém uma expressão regular que representa o padrão a ser correspondido. A segunda regra contém uma expressão regular que representa o texto de substituição. Você também deve criar um atributo [de destino Manipulation](/windows/desktop/Nps/sdo-manipulation-target) . Esse atributo é uma enumeração que especifica qual parte das informações do usuário deve ser manipulada.

A ordem na qual os atributos são criados é importante. O NPS processa os atributos na ordem em que foram criados.

A tabela a seguir mostra um exemplo de um conjunto de atributos de manipulação.



| Nome                 | Tipo         | Valor da cadeia de caracteres     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | "guest@"         |
| msManipulationTarget | **\_I4 VT**   | "1"              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hierarquia de modelo de objeto](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Atributos com suporte a SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Criando uma política de solicitação de conexão](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 