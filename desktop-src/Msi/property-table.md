---
description: A tabela de propriedades contém os nomes e valores de propriedade de todas as propriedades definidas na instalação. Propriedades com valores nulos não estão presentes na tabela.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabela de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662149"
---
# <a name="property-table"></a>Tabela de propriedades

A tabela de propriedades contém os nomes e valores de propriedade de todas as propriedades definidas na instalação. Propriedades com valores nulos não estão presentes na tabela.

A tabela de propriedades tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Valor    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

O nome de uma propriedade. Consulte [Propriedades](properties.md).

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Um valor de cadeia de caracteres localizável para a propriedade. Isso pode nunca ser nulo ou uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que você não pode usar a tabela de propriedades para definir uma propriedade para o valor de outra propriedade. O instalador não faz nada para a cadeia de caracteres de texto inserida na coluna valor antes de definir a propriedade na coluna propriedade. Se Firstproperty for inserido na coluna de propriedade e \[ segundoproperty \] na coluna Value, o valor de firstproperty será definido como a cadeia de texto " \[ secondproperty \] " e não com o valor da propriedade segundaproperty. Isso é necessário para evitar a criação de referências circulares na tabela de propriedades. Em vez disso, você pode definir uma propriedade para outra usando um [tipo de ação personalizada 51](custom-action-type-51.md).

Observe que a propriedade [**adminproperties**](adminproperties.md) pode ser usada para substituir os valores na tabela de propriedades durante uma [instalação administrativa](administrative-installation.md).

Não use Propriedades para senhas ou outras informações que devam permanecer seguras. O instalador pode gravar o valor de uma propriedade criada na tabela de propriedades ou criado em tempo de execução, em um log ou no registro do sistema.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



