---
description: A tabela MsiLockPermissionsEx pode ser usada para proteger serviços, arquivos, chaves do registro e pastas criadas.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabela MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759650"
---
# <a name="msilockpermissionsex-table"></a>Tabela MsiLockPermissionsEx

A tabela MsiLockPermissionsEx pode ser usada para proteger serviços, arquivos, chaves do registro e pastas criadas.

Um pacote não deve conter a tabela MsiLockPermissionsEx e a [Tabela LockPermissions](lockpermissions-table.md).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esta tabela é recomendada para pacotes destinados à instalação com o Windows Installer 5,0 ou posterior.

A tabela MsiLockPermissionsEx tem as colunas a seguir.



| Coluna               | Tipo                                       | Chave | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | S   | N        |
| LockObject           | [Identificador](identifier.md)               | N   | N        |
| Tabela                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Condição            | [Condição](condition.md)                 | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Esta é a chave primária desta tabela.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Essa coluna e a coluna da tabela juntas especificam o arquivo, o diretório, a chave do registro ou o serviço a ser protegido. A coluna lockobject é uma chave estrangeira que aponta para a chave primária da tabela especificada pela coluna da tabela.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Essa coluna e a coluna lockobject especificam o arquivo, o diretório, a chave do registro ou o serviço a ser protegido. Na coluna da tabela, insira arquivo, registro, CreateFolder ou instalar para especificar um lockobject listado na tabela de [arquivos](file-table.md), na [tabela do registro](registry-table.md), na tabela [CreateFolder](createfolder-table.md)ou na [tabela de instalação](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Insira a cadeia de caracteres SDDL para indicar as permissões a serem aplicadas ao objeto selecionado. O SDDL deve ser fornecido no [formato de cadeia de caracteres do descritor de segurança](../secauthz/security-descriptor-string-format.md).

Isso não oferece suporte a propriedades privadas ou públicas.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Esta coluna contém uma expressão condicional usada para determinar se a permissão especificada deve ser aplicada. Se a condição for avaliada como **false**, a permissão não será aplicada. Se a condição for avaliada como **true**, a permissão será aplicada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte [protegendo recursos](securing-resources-.md)para obter mais informações sobre como proteger serviços, arquivos, chaves do registro e pastas criadas.

Use a tabela MsiLockPermissionsEx para proteger objetos para uma conta de usuário que está sendo criada durante a instalação. A conta de usuário já deve existir quando a instalação proteger o objeto. Crie a conta de usuário antes de instalar o arquivo, a chave do registro, a pasta ou o serviço que está sendo protegido.

Se um lockobject e um par de tabelas nesta tabela tiverem mais de uma expressão condicional avaliada como true, a instalação falhará e Windows Installer retornará uma mensagem de erro 1942.

Se a cadeia de caracteres [FormattedSDDLText](formattedsddltext.md) no campo SDDLText não puder ser resolvida em uma cadeia de caracteres SDDL válida, a instalação falhará e Windows Installer retornará uma mensagem de erro 1943.

Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em um arquivo ou pasta, a instalação falhará e Windows Installer retornará uma mensagem de erro 1926.

Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em uma chave do registro, a instalação falhará e Windows Installer retornará uma mensagem de erro 1401.

Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em um serviço, a instalação falhará e Windows Installer retornará uma mensagem de erro 1944.

## <a name="validation"></a>Validação

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
