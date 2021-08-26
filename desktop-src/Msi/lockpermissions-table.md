---
description: Usado para proteger partes individuais de um aplicativo em um ambiente bloqueado. Ele pode ser usado com a instalação de arquivos, chaves do Registro e pastas criadas.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabela LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6724f9559f8bf4b5c0aac4581dab6ad7496e2c0e8e023636e621214760c26c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043136"
---
# <a name="lockpermissions-table"></a>Tabela LockPermissions

A Tabela LockPermissions é usada para proteger partes individuais de um aplicativo em um ambiente bloqueado. Ele pode ser usado com a instalação de arquivos, chaves do Registro e pastas criadas.

Um pacote destinado à instalação no Windows Server 2008 R2 ou Windows 7 deve usar a Tabela [MsiLockPermissionsEx em](msilockpermissionsex-table.md) vez da Tabela LockPermissions. Windows As versões do instalador anteriores Windows instalador 5.0 ignoram a tabela MsiLockPermissionsEx. Windows O Instalador 5.0 pode instalar um pacote que contém a Tabela LockPermissions. A partir do Windows Installer 5.0, a instalação de um pacote que contém a Tabela MsiLockPermissionsEx e a Tabela LockPermissions falha e retorna Windows mensagem de erro do Instalador 1941.

A Tabela LockPermissions tem as seguintes colunas.



| Coluna     | Tipo                               | Chave | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [Identificador](identifier.md)       | Y   | N        |
| Tabela      | [Text](text.md)                   | Y   | N        |
| Domínio     | [Formatado](formatted.md)         | Y   | Y        |
| Usuário       | [Formatado](formatted.md)         | Y   | N        |
| Permissão | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Essa coluna e a coluna Tabela especificam juntos o arquivo, o diretório ou a chave do Registro que deve ser protegida. A coluna LockObject é uma chave estrangeira que aponta para a chave primária da tabela especificada pela coluna Tabela.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Essa coluna e a coluna LockObject especificam o arquivo, o diretório ou a chave do Registro que deve ser protegida. Na coluna Tabela, insira Arquivo, Registro ou CreateFolder para especificar um LockObject listado na Tabela de Arquivos [,](file-table.md)Tabela do Registro [ou](registry-table.md) [CreateFolder Table](createfolder-table.md).

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domínio
</dt> <dd>

A coluna que identifica o domínio do usuário para o qual as permissões devem ser definidas. Esse é o nome de um computador autônomo ou um nome de domínio. O tipo de dados de coluna é [Formatado](formatted.md)e você pode usar a cadeia de caracteres %USERDOMAIN neste campo para obter o valor da variável de ambiente \[ \] USERDOMAIN para o domínio atual. Para obter qualquer outro domínio, é necessário usar [ações personalizadas.](custom-actions.md) Para obter mais informações, consulte a Tabela de Ações Personalizadas.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Usuário
</dt> <dd>

A coluna que identifica o nome localizado do usuário para o qual as permissões devem ser definidas. Esse nome deve estar localizado no computador ou domínio. A instalação falhará se o computador ou controlador de domínio não reconhecer a combinação de domínio e usuário ou se o SID (identificador de segurança) do usuário não puder ser recuperado. Vários usuários podem ser especificados para um único LockObject.

Os nomes de usuário comuns "Todos" e "Administradores" podem ser inseridos em inglês e mapeados para SIDs conhecidos. LocalSystem recebe controle total em todos os descritores de segurança criados por meio da Tabela LockPermissions. Você pode usar a propriedade [**ComputerName**](computername.md), [**a propriedade LogonUser**](logonuser.md) ou a propriedade [**USERNAME**](username.md) neste campo para obter o usuário atual. Uma ação personalizada é necessária para inserir o nome localizado de qualquer outro usuário ou grupo.

Você pode usar vários registros com entradas LockObject e Table idênticas (mas entradas de usuário diferentes) para especificar listas de controle de acesso para vários usuários.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permissão
</dt> <dd>

A coluna que identifica a descrição de inteiro dos privilégios do sistema. O exemplo a seguir fornece os valores mais usados (existe uma lista completa no Winnt.h).



| Privilege                                                              | Descrição                     |
|------------------------------------------------------------------------|---------------------------------|
| GENERIC \_ ALL<br/> 0X10000000<br/> 268435456<br/>     | Acesso de leitura, gravação e execução |
| EXECUÇÃO \_ GENÉRICA<br/> 0X20000000<br/> 536870912<br/> | Executar acesso                  |
| GRAVAÇÃO \_ GENÉRICA<br/> 0X40000000<br/> 1073741824<br/>  | Acesso de gravação                    |



 

Não é possível especificar GENERIC \_ READ na coluna Permissão. A tentativa de fazer isso falhará. Em vez disso, você deve especificar um valor como KEY \_ READ ou FILE GENERIC \_ \_ READ.

Nulo inserido nessa coluna é reservado para uso futuro.

</dd> </dl>

## <a name="remarks"></a>Comentários

As [ações InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)e [CreateFolders](createfolders-action.md) em tabelas de sequência [*processam*](s-gly.md) as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência,* [consulte Usando uma tabela de sequência](using-a-sequence-table.md).

A permissão só pode ser definida na Tabela LockPermissions para usuários que já existem no computador ou domínio. Uma tentativa de definir permissões para um usuário desconhecido faz com que a instalação falhe, mesmo que essa conta de usuário seja criada durante a instalação por uma ação personalizada adiada.

É recomendável que o grupo local do administrador do sistema seja incluído em todas as ACL (listas de controle de acesso). Isso garante que o administrador do sistema possa acessar e manter objetos.

Cada arquivo, chave do Registro ou diretório listado na Tabela LockPermissions recebe um descritor de segurança explícito, quer substitua um objeto existente ou não. O Windows instalador tenta preservar a segurança em objetos que já existem no sistema. Se um objeto não estiver listado na Tabela LockPermissions e substituir um objeto existente, a substituição obtém as configurações de segurança do objeto que ele substitui.

Se um objeto não estiver listado na Tabela LockPermissions e não substituir um objeto existente, ele não receberá nenhum descritor de segurança explícito. O acesso ao novo objeto baseia-se nos atributos de seu objeto pai ou contêiner. Se um objeto não estiver listado na tabela e substituir um objeto sem descritor de segurança explícito, o acesso ao novo objeto será baseado nos atributos de seu objeto pai ou contêiner.

O Windows instalador define a [**propriedade UserSID**](usersid.md) como o SID (identificador de segurança) ou o usuário que executa a instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




