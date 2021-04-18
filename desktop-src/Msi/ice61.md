---
description: ICE61 valida a tabela de atualização de um banco de dados Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752257"
---
# <a name="ice61"></a>ICE61

ICE61 verifica a tabela de atualização para garantir que as seguintes condições sejam verdadeiras:

-   Todas as propriedades Actionproperty não são previamente autorizadas na tabela de propriedades.
-   Todas as propriedades Actionproperty são propriedades públicas.
-   Todas as propriedades Actionproperty são incluídas na propriedade [**SecureCustomProperties**](securecustomproperties.md) .
-   Todas as propriedades Actionproperty são exclusivas para cada registro na tabela de atualização.
-   Todos os valores de VersionMax não são menores que os valores de VersionMin correspondentes.
-   Os valores VersionMin e VersionMax são versões válidas do produto. Consulte a propriedade [**ProductVersion**](productversion.md) para obter o formato de versão de produto válido.
-   Nenhuma tentativa é feita para remover uma versão mais recente ou igual do produto atual.

Falha ao corrigir um aviso ou erro relatado por ICE61 geralmente leva a problemas na atualização do aplicativo. Dependendo do erro exato, isso pode ser qualquer coisa desde deixar arquivos da versão mais antiga por trás, excluir arquivos da versão mais antiga, mesmo que sejam necessários para o novo aplicativo ou concluir a falha da atualização.

## <a name="result"></a>Resultado

ICE61 posta um aviso ou erro se qualquer uma das condições acima não for verdadeira.

## <a name="example"></a>Exemplo

ICE61 relata os erros e avisos a seguir para os exemplos mostrados.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

Nesse caso, a primeira linha tentaria remover um produto da mesma versão. (A coluna VersionMax é igual à versão do produto na tabela de propriedades).

Para corrigir esse erro, use uma versão na coluna VersionMax inferior à versão atual especificada na tabela de propriedades. Remova o bit **msidbUpgradeAttributesVersionMaxInclusive** da coluna atributos se o VersionMax for igual à versão atual. Se a intenção for apenas detectar o produto e não removê-lo, adicionar o bit **msidbUpgradeAttributesOnlyDetect** à coluna atributos também corrigirá esse erro.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A menos que a propriedade esteja listada na propriedade [**SecureCustomProperties**](securecustomproperties.md) , a propriedade não será passada para o lado do servidor da instalação quando a propriedade for encontrada.

Para corrigir esse erro, adicione a propriedade a [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

As propriedades de atualização devem ser propriedades públicas para que o resultado seja passado para o lado do servidor da instalação.

Para corrigir esse erro, use todas as letras maiúsculas no nome da propriedade.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Uma propriedade só pode ser usada em uma linha da tabela de atualização.

Para corrigir esse erro, use uma propriedade diferente para a segunda linha.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

A versão mínima deve ser menor que a versão máxima.

Para corrigir esse erro, verifique se há erros de digitação nos números de versão. Se eles estiverem corretos e você quiser usar o intervalo entre as duas versões, alterne-as para que VersionMin seja menor que VersionMax.

[Tabela de propriedades](property-table.md)



| Propriedade                                                 | Valor                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Atualizar tabela](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos | Remover                | Açãoproperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1046     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



