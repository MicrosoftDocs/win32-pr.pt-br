---
description: O ICE61 valida a tabela Atualizar de um banco de Windows do Instalador.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c772a076decaa385d01047daa45871aeeaf7898d4cf3347606c4066d1f7f2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580976"
---
# <a name="ice61"></a>ICE61

O ICE61 verifica a tabela de atualização para garantir que as seguintes condições sejam verdadeiras:

-   Todas as propriedades actionProperty não são pré-autoradas na tabela Property.
-   Todas as propriedades ActionProperty são Propriedades Públicas.
-   Todas as propriedades ActionProperty estão incluídas na [**propriedade SecureCustomProperties.**](securecustomproperties.md)
-   Todas as propriedades ActionProperty são exclusivas para cada registro na tabela Upgrade.
-   Todos os valores versionmax não são menores que os valores de VersionMin correspondentes.
-   Os valores VersionMin e VersionMax são versões válidas do produto. Consulte a [**propriedade ProductVersion**](productversion.md) para o formato de versão do produto válido.
-   Nenhuma tentativa é feita para remover uma versão mais recente ou igual do produto atual.

A falha na correção de um aviso ou erro relatado pelo ICE61 geralmente leva a problemas ao atualizar seu aplicativo. Dependendo do erro exato, isso pode ser qualquer coisa desde deixar arquivos da versão mais antiga para trás, excluir arquivos da versão mais antiga, mesmo que eles sejam necessários para o novo aplicativo ou falha completa da atualização.

## <a name="result"></a>Resultado

ICE61 postará um aviso ou erro se qualquer uma das condições acima não for verdadeira.

## <a name="example"></a>Exemplo

O ICE61 relata os seguintes erros e avisos para os exemplos mostrados.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

Nesse caso, a primeira linha tentará remover um produto da mesma versão. (A coluna VersionMax é igual à versão do produto na tabela Propriedade).

Para corrigir esse erro, use uma versão na coluna VersionMax inferior à versão atual especificada na tabela Property. Remova o **bit msidbUpgradeAttributesVersionMaxInclusive** da coluna Atributos se VersionMax for igual à versão atual. Se a intenção for apenas detectar o produto e não removê-lo, adicionar o bit **msidbUpgradeAttributesOnlyDetect** à coluna Atributos também corrigirá esse erro.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A menos que a propriedade esteja listada na propriedade [**SecureCustomProperties,**](securecustomproperties.md) a propriedade não será passada para o lado do servidor da instalação quando a propriedade for encontrada.

Para corrigir esse erro, adicione a propriedade [**a SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

As propriedades de atualização devem ser propriedades públicas para que o resultado seja passado para o lado do servidor da instalação.

Para corrigir esse erro, use todas as letras maiúsculas no nome da propriedade.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Uma propriedade só pode ser usada em uma linha da tabela Upgrade.

Para corrigir esse erro, use uma propriedade diferente para a segunda linha.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

A versão mínima deve ser menor que a versão máxima.

Para corrigir esse erro, verifique os números de versão para erros de digitação. Se eles estão corretos e você deseja usar o intervalo entre as duas versões, alternar para que VersionMin seja menor que VersionMax.

[Tabela de propriedades](property-table.md)



| Propriedade                                                 | Valor                                  |
|----------------------------------------------------------|----------------------------------------|
| [**Upgradecode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**Productversion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Atualizar tabela](upgrade-table.md)



| Upgradecode                            | VersionMin | VersionMax | Idioma | Atributos | Remover                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1046     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



