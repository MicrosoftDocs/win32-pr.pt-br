---
description: Os nomes das chaves primárias de um banco de dados de módulo de mesclagem devem aderir a uma convenção de nomenização padrão.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Nomeando chaves primárias em bancos de dados de módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ab2f7dbb5a41f5999271e5c679b67c6ee37d9b79302509ef61e9dbca97894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627804"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Nomeando chaves primárias em bancos de dados de módulo de mesclagem

Os nomes das chaves primárias de um banco de dados de módulo de mesclagem devem aderir a uma convenção de nomenização padrão. A finalidade dessa convenção de nomenculação é reduzir a possibilidade de criar um conflito de nome entre as colunas de tabela no módulo de mesclagem e o pacote de instalação de destino. A convenção de nomen efetivação não pode ser aplicada a tabelas nas quais a chave primária é um dado que pode ser instalado. Não aplique a convenção de nomen entre as seguintes tabelas:

-   [Tabela MIME](mime-table.md)
-   [Tabela de extensão](extension-table.md)
-   [Tabela de ícones](icon-table.md)
-   [Tabela de verbos](verb-table.md)
-   [Tabela ProgId](progid-table.md)

Por exemplo, não use para a chave primária da tabela MIME porque esse é o tipo MIME e aplicar o procedimento de nomenal alteraria seu significado. Nesses casos, os conflitos de nome dependem do significado dos dados serem exclusivos entre módulos.

O nome de uma chave primária em um módulo de mesclagem deve consistir em um nome acessível anexado com uma cadeia de caracteres feita do GUID do módulo de mesclagem. Cada módulo de mesclagem deve ter seu [*próprio GUID.*](g-gly.md) O GUID do módulo de mesclagem também deve ser autor da propriedade [**Resumo do**](revision-number-summary.md) Número de Revisão do módulo de mesclagem. Os desenvolvedores podem criar GUIDs usando um utilitário como GUIDGEN.

O procedimento a seguir descreve como gerar uma chave de banco de dados primária que adere à convenção de nomenal padrão. Aplique o procedimento a seguir somente a tabelas em que a chave primária não está sendo instalada.

**Para nomear uma chave primária de um registro de tabela em um módulo de mesclagem**

1.  Autor da parte acessível do nome da chave primária. Escolha um nome acessível que identifique esse registro, por exemplo, MyRowEntry.
2.  Gere ou obtenha o GUID do módulo de mesclagem. Observe que todos os GUIDs devem ser autorados em letras maiúsculas. Para obter mais informações sobre GUIDs, consulte [GUID](guid.md). Veja a seguir um exemplo de um GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. Nas etapas a seguir, você modifica isso em uma cadeia de caracteres que deve ser anexada a cada nome de chave primária no módulo de mesclagem.
3.  Remova as chaves do início e do fim do GUID.
4.  Altere todos os traços para sublinhados.
5.  Anexar o resultado ao final da parte acessível do nome da chave primária. Separe o nome acessível do GUID modificado por um ponto. O nome da chave primária para o GUID de exemplo acima é MyRowEntry.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Repita para nomear todas as chaves primárias de todas as tabelas no módulo de mesclagem.

 

 



