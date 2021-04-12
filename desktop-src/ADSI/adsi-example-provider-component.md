---
title: Componente do provedor de exemplo ADSI
description: Active Directory escritores de provedor de interfaces de serviço encontrarão esta seção de interesse específico, pois ela descreve o componente de exemplo de provedor ADSI em detalhes.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291802"
---
# <a name="adsi-example-provider-component"></a>Componente do provedor de exemplo ADSI

Active Directory escritores de provedor de interfaces de serviço encontrarão esta seção de interesse específico, pois ela descreve o componente de exemplo de provedor ADSI em detalhes. Os gravadores do provedor ADSI podem instalar o provedor de exemplo e usar a estrutura de código como uma base para criar sua própria implementação. Os seguintes tópicos são abordados:

[A instalação do componente de provedor de exemplo](installing-the-example-provider-component.md) descreve como instalar o provedor de exemplo ADSI e seu diretório fictício. Esta seção inclui uma lista das configurações do registro.

[Definição de diretório](directory-definition.md) descreve as entradas de diretório definidas pelo componente de provedor de exemplo.

O [Gerenciamento de esquema](schema-management.md) descreve como cada elemento no exemplo de serviço de diretório de componente do provedor pode ser representado por um tipo específico de Active Directory objeto.

A [associação a um objeto Active Directory](binding-to-an-active-directory-object.md) descreve como, dada uma cadeia de caracteres ADsPath, o componente de provedor de exemplo identifica esse elemento, cria o tipo apropriado de objeto Active Directory para ele e recupera o tipo solicitado de ponteiro de interface nesse objeto para que ele passe de volta para o software cliente do ADS.

[Objetos de enumerador](enumerator-objects.md) lista os tipos específicos de enumerações fornecidos pelo componente de provedor de exemplo e em que código-fonte as implementações podem ser encontradas.

[Visão geral de código](code-overview.md) fornece uma descrição em nível de tarefa de cada parte do componente de provedor de exemplo.

[Detalhes do código](code-details.md) lista os módulos de software e seu conteúdo.

 

 




