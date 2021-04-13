---
description: A tabela de atualização contém as informações necessárias durante as atualizações principais.
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: Atualizar tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b48ce49f0f931209ccf472cd74b352c270353a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297441"
---
# <a name="upgrade-table"></a>Atualizar tabela

A tabela de atualização contém as informações necessárias durante as [atualizações principais](major-upgrades.md). Para habilitar totalmente os recursos de atualização do instalador, cada pacote deve ter uma propriedade [**UpgradeCode**](upgradecode.md) e uma tabela de atualização. Cada registro na tabela de atualização fornece uma combinação característica do código de atualização, da versão do produto e das informações de idioma usadas para identificar um conjunto de produtos afetados pela atualização. Quando a ação [FindRelatedProducts](findrelatedproducts-action.md) detecta um produto afetado instalado no sistema, ele anexa o código do produto a uma propriedade especificada na coluna actionproperty. A ação [RemoveExistingProducts](removeexistingproducts-action.md) e a ação [MigrateFeatureStates](migratefeaturestates-action.md) apenas removem ou migram produtos listados na coluna actionproperty.

A tabela de atualização contém as colunas mostradas na tabela a seguir.



| Coluna         | Tipo                         | Chave | Nullable |
|----------------|------------------------------|-----|----------|
| UpgradeCode    | [GUID](guid.md)             | S   | N        |
| VersionMin     | [Text](text.md)             | S   | S        |
| VersionMax     | [Text](text.md)             | S   | S        |
| Idioma       | [Text](text.md)             | S   | S        |
| Atributos     | [Inteiro](integer.md)       | S   | N        |
| Remover         | [Binário](formatted.md)   | N   | S        |
| Açãoproperty | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode
</dt> <dd>

A propriedade [UpgradeCode](upgradecode.md) nessa coluna especifica o código de atualização de todos os produtos que devem ser detectados pela ação [FindRelatedProducts](findrelatedproducts-action.md) .

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin
</dt> <dd>

Limite inferior do intervalo de versões de produto detectadas pelo [FindRelatedProducts](findrelatedproducts-action.md). Insira **msidbUpgradeAttributesVersionMinInclusive** em atributos para incluir VersionMin no intervalo. Se VersionMin for igual a uma cadeia de caracteres vazia (""), ela será avaliada da mesma forma que 0. Se VersionMin for NULL, FindRelatedProducts ignorará **msidbUpgradeAttributesVersionMinInclusive** e detectará todas as versões anteriores. VersionMin e VersionMax não devem ser ambos nulos.

VersionMin deve ser uma versão de produto válida, conforme descrito para a propriedade [**ProductVersion**](productversion.md) . Observe que Windows Installer usa apenas os três primeiros campos da versão do produto. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax
</dt> <dd>

Limite superior do intervalo de versões de produto detectadas pela ação [FindRelatedProducts](findrelatedproducts-action.md) . Insira **msidbUpgradeAttributesVersionMaxInclusive** em atributos para incluir VersionMax no intervalo. Se VersionMax for uma cadeia de caracteres vazia (""), ela será avaliada da mesma forma que 0. Se VersionMax for NULL, FindRelatedProducts ignorará **msidbUpgradeAttributesVersionMaxInclusive** e detectará todas as versões de produto maiores que (ou maior ou igual a) o limite inferior especificado por VersionMin e **msidbUpgradeAttributesVersionMinInclusive**. VersionMin e VersionMax não devem ser ambos nulos.

VersionMax deve ser uma versão de produto válida, conforme descrito para a propriedade [**ProductVersion**](productversion.md) . Observe que Windows Installer usa apenas os três primeiros campos da versão do produto. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

O conjunto de idiomas detectados pelo [FindRelatedProducts](findrelatedproducts-action.md). Insira uma lista de identificadores de idioma numéricos (LANGid) separados por vírgulas. Insira **msidbUpgradeAttributesLanguagesExclusive** em atributos para detectar todos os idiomas exclusivos daqueles listados em idioma. Se Language for NULL ou uma cadeia de caracteres vazia (""), FindRelatedProducts ignorará **msidbUpgradeAttributesLanguagesExclusive** e detectará todos os idiomas.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta coluna contém sinalizadores de bits que especificam atributos da tabela de atualização.



| Nome do sinalizador de bit                                 | Decimal | Hexadecimal | Atributo                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | Migra os Estados do recurso habilitando a lógica na ação [MigrateFeatureStates](migratefeaturestates-action.md) . |
| **msidbUpgradeAttributesOnlyDetect**          | 2       | 0x002       | Detecta produtos e aplicativos, mas não remove.                                                               |
| **msidbUpgradeAttributesIgnoreRemoveFailure** | 4       | 0x004       | Continua a instalação após a falha ao remover um produto ou aplicativo.                                              |
| **msidbUpgradeAttributesVersionMinInclusive** | 256     | 0x100       | Detecta o intervalo de versões, incluindo o valor em VersionMin.                                                     |
| **msidbUpgradeAttributesVersionMaxInclusive** | 512     | 0x200       | Detecta o intervalo de versões, incluindo o valor em VersionMax.                                                     |
| **msidbUpgradeAttributesLanguagesExclusive**  | 1024    | 0x400       | Detecta todos os idiomas, excluindo os idiomas listados na coluna idioma.                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>Exclu
</dt> <dd>

O instalador define a propriedade [**Remove**](remove.md) para os recursos especificados nesta coluna. Os recursos a serem removidos podem ser determinados em tempo de execução. A cadeia de caracteres [formatada](formatted.md) inserida neste campo deve ser avaliada como uma lista delimitada por vírgulas de nomes de recursos. Por exemplo: \[ Feature1 \] , \[ Feature2 \] , \[ Feature3 \] . Nenhum recurso será removido se o campo contiver texto formatado que seja avaliado como uma cadeia de caracteres vazia (""). O instalador define REMOVE = ALL somente se o campo remove estiver vazio. Observe a diferença entre uma cadeia de caracteres vazia e um campo vazio. Se o campo estiver vazio, ele será nulo.

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>Açãoproperty
</dt> <dd>

Quando a ação [FindRelatedProducts](findrelatedproducts-action.md) detecta um produto relacionado instalado no sistema, ele anexa o código do produto à propriedade especificada neste campo. A propriedade especificada nesta coluna deve ser uma propriedade pública e o autor do pacote deve adicionar a propriedade à propriedade [**SecureCustomProperties**](securecustomproperties.md) . Cada linha na tabela de atualização deve ter um valor Actionproperty exclusivo. Após FindRelatedProducts, o valor dessa propriedade é uma lista de códigos de produto, separados por ponto-e-vírgula (;), detectado no sistema.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 



