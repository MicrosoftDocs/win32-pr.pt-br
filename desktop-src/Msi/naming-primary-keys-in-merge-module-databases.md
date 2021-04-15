---
description: Os nomes das chaves primárias que um banco de dados de módulo de mesclagem devem aderir a uma Convenção de nomenclatura padrão.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Nomeando chaves primárias em bancos de dados do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502364"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Nomeando chaves primárias em bancos de dados do módulo de mesclagem

Os nomes das chaves primárias que um banco de dados de módulo de mesclagem devem aderir a uma Convenção de nomenclatura padrão. A finalidade dessa Convenção de nomenclatura é reduzir a possibilidade de criar um conflito de nome entre as colunas da tabela no módulo de mesclagem e o pacote de instalação de destino. A Convenção de nomenclatura não pode ser aplicada a tabelas nas quais a chave primária é dados instaláveis. Não aplique a Convenção de nomenclatura às seguintes tabelas:

-   [Tabela MIME](mime-table.md)
-   [Tabela de extensão](extension-table.md)
-   [Tabela de ícones](icon-table.md)
-   [Tabela de verbo](verb-table.md)
-   [Tabela ProgId](progid-table.md)

Por exemplo, não use para a chave primária da tabela MIME porque esse é o tipo MIME e a aplicação do procedimento de nomenclatura alteraria seu significado. Nesses casos, os conflitos de nome dependem do significado dos dados que são exclusivos entre os módulos.

O nome de uma chave primária em um módulo de mesclagem deve consistir em um nome legível anexado a uma cadeia de caracteres feita a partir do GUID do módulo de mesclagem. Cada módulo de mesclagem deve ter seu próprio [*GUID*](g-gly.md). O GUID do módulo de mesclagem também deve ser criado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do módulo de mesclagem. Os desenvolvedores podem criar GUIDs usando um utilitário como o GUIDGEN.

O procedimento a seguir descreve como gerar uma chave de banco de dados primária que segue a Convenção de nomenclatura padrão. Aplique o procedimento a seguir somente a tabelas em que a chave primária não está sendo instalada dados.

**Para nomear uma chave primária de um registro de tabela em um módulo de mesclagem**

1.  Crie a parte legível do nome para a chave primária. Escolha um nome legível que identifique esse registro, por exemplo, MyRowEntry.
2.  Gerar ou obter o GUID do módulo de mesclagem. Observe que todos os GUIDs devem ser criados em letras maiúsculas. Para obter mais informações sobre GUIDs, consulte [GUID](guid.md). Veja a seguir um exemplo de um GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. Nas etapas a seguir, você pode modificar isso em uma cadeia de caracteres que deve ser anexada a cada nome de chave primária no módulo de mesclagem.
3.  Remova as chaves do início e do fim do GUID.
4.  Altere todos os traços para sublinhados.
5.  Acrescente o resultado ao final da parte legível do nome da chave primária. Separe o nome legível do GUID modificado por um ponto. O nome da chave primária para o GUID de exemplo fornecido acima torna-se MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Repita para nomear todas as chaves primárias de todas as tabelas no módulo de mesclagem.

 

 



