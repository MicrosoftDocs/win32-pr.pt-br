---
title: Modelo de esquema ADSI
description: Um esquema é semelhante a um dicionário no qual contém a definição de cada tipo de objeto conhecido por um serviço de diretório.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI do modelo de esquema ADSI
- ADSI ADSI, sobre, esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4893151c81eefa0a17420e18d5d87da232641571
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883874"
---
# <a name="adsi-schema-model"></a>Modelo de esquema ADSI

Um esquema é semelhante a um dicionário no qual contém a definição de cada tipo de objeto conhecido por um serviço de diretório. Os aplicativos cliente ADSI podem navegar por um esquema para descobrir os recursos de qualquer implementação adsi. Além disso, a ADSI fornece interfaces de gerenciamento de esquema que podem ser usadas para se comunicar com o esquema subjacente de um serviço de diretório.

Alguns esquemas são extensíveis e provedores ADSI ou fornecedores de terceiros podem optar por publicar novas interfaces ou propriedades adicionais para interfaces existentes. Os clientes ADSI usam esses dados para determinar quais recursos têm suporte para cada serviço de diretório.

Há três tipos de objetos de esquema: classes, propriedades e sintaxes, cada um dando suporte, respectivamente, às interfaces de gerenciamento de esquema [**IADsClass,**](/windows/desktop/api/Iads/nn-iads-iadsclass) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

> [!Note]  
> Classe é um termo sobrecarregado. Há classes C++, classes Java, classes COM e classes ADSI. Neste documento, a classe de palavra, a menos que qualificada de outra forma, refere-se a uma categoria ou tipo de objeto de esquema.

 

A ADSI abstrai o esquema de cada serviço de diretório e o coloca em cada nó raiz de nível superior no **objeto Namespace.** Para identificar quais classes um serviço de diretório dá suporte em um determinado nó raiz, você enumera o objeto de esquema e obter uma lista de objetos de classe, objetos de propriedade e objetos de sintaxe. Para obter mais informações, [consulte Usando o esquema ADSI](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Cache de esquema do provedor ADSI LDAP

O provedor LDAP para ADSI tenta armazenar dados de esquema em cache no computador local. Um subesquipe é identificado por um nome diferenciado armazenado no atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) localizado na raiz do serviço de diretório enterprise (rootDSE). Além de fornecer os dados de subschema, os servidores LDAP v3 devem expor um atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) usado para determinar a última vez em que o esquema foi modificado.

Quando o ADSI se vincula pela primeira vez ao servidor LDAP, ele recupera os dados de subschema usando o [**atributo subSchemaSubEntry.**](/windows/desktop/ADSchema/a-subschemasubentry) Se o ADSI tiver êxito ao localizar o objeto de subschema, ele armazenará um ponteiro para os dados no Registro no computador que está se conectando ao servidor LDAP. Para obter informações sobre exatamente onde esses valores são armazenados no Registro, consulte [ADSI e Controle de Conta de Usuário](adsi-and-uac.md).

A ADSI tenta processar os dados de esquema e lê o [**atributo modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Se o atributo **modifyTimeStamp** existir e ADSI processa com êxito o esquema, a ADSI grava o subesquisquia no disco e cria os dois valores de Registro a seguir na chave. Se os dados de subschema existirem, mas não puderem ser processados, nenhum desses valores de Registro será criado:

-   Um **valor** time, que contém o [**atributo modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Esse valor é usado para garantir que os dados de esquema são atuais e impede o recarregamento constante dos dados do esquema.
-   Um **valor** de Arquivo, que contém o caminho para onde a ADSI armazena os dados de esquema no sistema de arquivos. Por padrão, a ADSI armazena em cache o subesquipe no diretório Systemroot SchCache com um nome de arquivo correspondente ao nome &lt; &gt; \\ do servidor LDAP.

Se os dados de subschema puderem ser processados, mas nenhum atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) for exposto, os dados de esquema serão armazenados em cache na memória, mas não gravados em disco. Se um servidor LDAP v3 tiver sido contatado por meio da ADSI no computador local e um subesquisquia armazenado em cache não estiver presente, provavelmente será por um dos seguintes motivos:

-   O servidor não expôs as propriedades corretas.
-   ADSI não pôde processar o esquema.
-   ADSI não pôde gravar o arquivo no sistema de arquivos.

 

 
