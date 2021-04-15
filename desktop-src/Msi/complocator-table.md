---
description: A tabela CompLocator contém as informações necessárias para localizar um arquivo ou diretório que está usando os dados de configuração do instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabela CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506256"
---
# <a name="complocator-table"></a>Tabela CompLocator

A tabela CompLocator contém as informações necessárias para localizar um arquivo ou diretório que está usando os dados de configuração do instalador.

A tabela CompLocator contém as informações a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificador](identifier.md) | S   | N        |
| ComponentId | [GUID](guid.md)             | N   | N        |
| Tipo        | [Inteiro](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informações da coluna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

Essa coluna representa uma assinatura de arquivo exclusiva e também a chave externa na [tabela de assinatura](signature-table.md). Se a chave estiver ausente da tabela de assinatura, a pesquisa será considerada para a presença de um diretório apontado pela tabela CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

A ID do componente cujo caminho de chave deve ser usado para a pesquisa. Deve ser o GUID de um componente que aparece no campo ComponentID da [tabela de componentes](component-table.md). Pode ser a ID do componente de um componente pertencente a outro produto instalado no computador. Ele não deve ser o GUID de um componente publicado que aparece no campo ComponentID da [tabela PublishComponent](publishcomponent-table.md).

Para localizar o valor de GUID de ID de componente para um arquivo instalado por outro produto, vá para o pacote de instalação do produto. Vá para a [tabela de arquivos](file-table.md) e localize a linha que contém o identificador de arquivo para o arquivo. A \_ coluna Component dessa linha contém o identificador de componente para o componente que controla o arquivo. Vá para a [tabela de componentes](component-table.md) e localize a linha que contém esse identificador de componente na coluna componente. A coluna ComponentID desta linha contém o GUID da ID do componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

Um valor booliano que determina se o caminho de chave do componente é um nome de arquivo ou um local de diretório.

A tabela a seguir lista os valores válidos. Se estiver ausente, o tipo será definido como 1 (um).



| Constante                      | Hexadecimal | Decimal | Descrição              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | O caminho da chave é um diretório. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | O caminho da chave é um nome de arquivo. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).

Normalmente, as colunas nesta tabela não são localizadas. Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

Para obter mais informações, consulte [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



