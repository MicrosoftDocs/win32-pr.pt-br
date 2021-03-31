---
description: O ICE46 verifica as propriedades personalizadas em condições, texto formatado e outros locais que diferem de uma propriedade definida pelo sistema somente pelo caso de um ou mais caracteres.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662063"
---
# <a name="ice46"></a>ICE46

O ICE46 verifica as propriedades personalizadas em condições, texto formatado e outros locais que diferem de uma propriedade definida pelo sistema somente pelo caso de um ou mais caracteres.

## <a name="result"></a>Resultado

O ICE46 posta uma mensagem informativa se houver uma propriedade personalizada em uma condição, um texto formatado e outro local que seja diferente de propriedades definidas pelo sistema somente no caso de um ou mais caracteres.

## <a name="example"></a>Exemplo

ICE46 relata os erros a seguir para o exemplo mostrado.



| Erro de ICE46                                                                                                                                            | Descrição                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A propriedade REINSTALLMODE definida na tabela de propriedades difere de outra propriedade definida somente por maiúsculas e minúsculas.                                                   | O nome da propriedade definida pelo sistema **REinstallmode** difere da propriedade personalizada somente por caso. As propriedades diferenciam maiúsculas de minúsculas, portanto, a propriedade personalizada não é a mesma que a propriedade do sistema. Essa é uma causa comum de erros. |
| Propriedade ' MyProperty ' referenciada na coluna ' InstallExecuteSequence '. ' A condição ' da linha ' InstallFinalize ' difere de uma propriedade definida somente por caso. | A tabela de propriedades define a tabela MyProperty, mas a propriedade referenciada é MyProperty. As propriedades diferenciam maiúsculas de minúsculas, portanto, as duas propriedades não são as mesmas. Essa é uma causa comum de erros.                          |



 

[Tabela de propriedades](property-table.md)



| Propriedade      | Valor   |
|---------------|---------|
| ReinstallMode | omus    |
| MyProperty    | um valor |



 

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação          | Condição  |
|-----------------|------------|
| InstallFinalize | Myproperty |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



