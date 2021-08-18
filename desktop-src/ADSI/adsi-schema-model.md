---
title: Modelo de esquema ADSI
description: Um esquema é semelhante a um dicionário, pois ele contém a definição de cada tipo de objeto conhecido por um serviço de diretório.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI do modelo de esquema ADSI
- ADSI ADSI, sobre, esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd8c06d10e05c11b2cc7c578814bb4ded2d897d3b7913b9b3d341a8a6c49086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023744"
---
# <a name="adsi-schema-model"></a>Modelo de esquema ADSI

Um esquema é semelhante a um dicionário, pois ele contém a definição de cada tipo de objeto conhecido por um serviço de diretório. Os aplicativos cliente ADSI podem navegar por um esquema para descobrir os recursos de qualquer implementação ADSI específica. Além disso, a ADSI fornece interfaces de gerenciamento de esquema que podem ser usadas para se comunicar com o esquema subjacente de um serviço de diretório.

Alguns esquemas são provedores extensíveis e ADSI ou fornecedores de terceiros podem optar por publicar novas interfaces ou propriedades adicionais para interfaces existentes lá. Os clientes ADSI usam esses dados para determinar quais recursos têm suporte para cada serviço de diretório.

Há três tipos de objetos de esquema: classes, propriedades e sintaxes, cada um respectivamente dando suporte às interfaces de gerenciamento de esquema [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

> [!Note]  
> A classe é um termo sobrecarregado. Há classes C++, classes Java, classes COM e classes ADSI. Neste documento, a palavra classe, a menos que qualificado de outra forma, se refere a uma categoria ou tipo de objeto de esquema.

 

A ADSI abstrai o esquema de cada serviço de diretório e o coloca em cada nó raiz de nível superior no objeto **namespace** . Para identificar as classes que um serviço de diretório dá suporte em um determinado nó raiz, você enumera o objeto de esquema e obtém uma lista de objetos de classe, objetos de propriedade e objetos de sintaxe. Para obter mais informações, consulte [usando o esquema ADSI](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Cache de esquema do provedor LDAP ADSI

O provedor LDAP para ADSI tenta armazenar em cache os dados de esquema no computador local. Um subesquema é identificado por um nome distinto armazenado no atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) localizado na raiz do serviço de diretório Enterprise (RootDSE). Além de fornecer os dados de subesquema, os servidores LDAP v3 devem expor um atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) que é usado para determinar a última vez em que o esquema foi modificado.

Quando o ADSI primeiro liga ao servidor LDAP, ele recupera os dados do subesquema usando o atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) . Se o ADSI obtiver sucesso ao localizar o objeto de subesquema, ele armazenará um ponteiro para os dados no registro no computador que está se conectando ao servidor LDAP. Para obter informações sobre exatamente onde esses valores são armazenados no registro, consulte [ADSI e controle de conta de usuário](adsi-and-uac.md).

Em seguida, o ADSI tenta processar os dados do esquema e lê o atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Se o atributo **modifyTimeStamp** existir e a ADSI processar o esquema com êxito, a ADSI gravará o subesquema em disco e criará os dois valores de registro a seguir sob a chave. Se os dados do subesquema existirem, mas não puderem ser processados, nenhum desses valores de registro será criado:

-   Um valor de **hora** , que contém o atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Esse valor é usado para garantir que os dados do esquema sejam atuais e impeçam o recarregamento constante dos dados do esquema.
-   Um valor de **arquivo** , que contém o caminho para onde a ADSI armazena os dados de esquema no sistema de arquivos. Por padrão, a ADSI armazena em cache o subesquema no <systemroot> \\ diretório SchCache com um nome de arquivo correspondente ao nome do servidor LDAP.

Se os dados do subesquema puderem ser processados, mas nenhum atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) for exposto, os dados do esquema serão armazenados em cache na memória, mas não gravados no disco. Se um servidor LDAP v3 tiver sido contatado por meio de ADSI no computador local e um subesquema em cache não estiver presente, provavelmente haverá um dos seguintes motivos:

-   O servidor não expôs as propriedades corretas.
-   A ADSI não pôde processar o esquema.
-   A ADSI não pôde gravar o arquivo no sistema de arquivos.

 

 