---
description: A tabela de ambiente é usada para definir os valores de variáveis de ambiente.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Tabela de ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de1fe52e8222bfde3e451b6ccc543511822e0d511a2ce1ce2b6bee8bc4fd117f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129596"
---
# <a name="environment-table"></a>Tabela de ambiente

A tabela de ambiente é usada para definir os valores de variáveis de ambiente.

A tabela de ambiente tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Ambiente | [Identificador](identifier.md) | Y   | N        |
| Nome        | [Text](text.md)             | N   | N        |
| Valor       | [Binário](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Ambiente
</dt> <dd>

Essa é a chave primária da tabela e é um token não localizado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Essa coluna é o nome localizável da variável de ambiente. Os valores de chave são gravados ou removidos, dependendo de quais dos caracteres na tabela a seguir são prefixados para o nome. Não há nenhum efeito na ordenação dos símbolos usados em um prefixo.



| Prefixo                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Crie a variável de ambiente se ela não existir e defina-a durante a instalação. Se a variável de ambiente existir, defina-a durante a instalação.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Crie a variável de ambiente, caso ela não exista, e defina-a durante a instalação. Isso não tem efeito sobre o valor da variável de ambiente, se já existir.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Remova a variável de ambiente quando o componente for removido. Esse símbolo pode ser combinado com qualquer prefixo.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Remova a variável de ambiente durante uma instalação. O instalador removerá apenas uma variável de ambiente durante uma instalação se o nome e o valor da variável corresponderem às entradas nos campos nome e valor da tabela de ambiente. Se você quiser remover uma variável de ambiente, independentemente de seu valor, use a sintaxe '! ' e deixe o campo de valor vazio.                                                                                                                    |
| \*                             | esse prefixo é usado com Windows 2000 para indicar que o nome se refere a uma variável de ambiente do sistema. Se nenhum asterisco estiver presente, o instalador gravará a variável no ambiente do usuário. Esse símbolo pode ser combinado com qualquer prefixo. Um pacote que é usado para instalação no [contexto de instalação](installation-context.md) por máquina deve gravar variáveis de ambiente no ambiente da máquina, incluindo \* na coluna nome. Para obter mais informações, consulte Comentários. |
| =-                             | A variável de ambiente é definida em instalar e removida na desinstalação. Esse é o comportamento usual.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Remove uma variável de ambiente durante uma instalação ou desinstalação.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Estes não são prefixos válidos                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Se o campo valor na tabela incluir um \[ ~ \] , os caracteres de prefixo se aplicarão apenas à parte especificada da cadeia de caracteres. O uso de \[ ~ \] é descrito abaixo na seção coluna de valor.

A variável de ambiente será removida se o campo de valor da tabela estiver em branco. Portanto, com um espaço em branco no campo value, um = prefix exclui a variável de ambiente em Install e um-prefix exclui quaisquer valores atuais na desinstalação.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta coluna contém o valor localizável que deve ser definido como uma cadeia de caracteres formatada. Consulte [formatado](formatted.md). Se esse campo for deixado em branco, a variável será removida. Se o campo estiver em branco e a cadeia de caracteres no campo nome for prefixada pelo símbolo, a variável será removida somente quando o componente for removido.

Para acrescentar um valor ao final de uma variável existente, Prefixe a cadeia de caracteres nesse campo pelo caractere nulo \[ ~ \] e pelo caractere separador. Por exemplo, se o ponto e vírgula for o separador escolhido: \[ ~ \] ;*Valor*.

Para prefixar um valor para a frente de uma variável existente, acrescente a cadeia de caracteres nesse campo pelo caractere separador e o caractere nulo \[ ~ \] . Por exemplo, se o ponto e vírgula for o separador escolhido: *valor*; \[ ~ \] .

Se não houver um \[ ~ \] presente no campo, a cadeia de caracteres representará o valor inteiro a ser definido ou excluído.

Cada linha pode conter apenas um valor. Por exemplo, o *valor* de entrada; *Valor* \[ ~ ; \] é maior que um valor e não deve ser usado porque causa resultados imprevisíveis. O *valor* da entrada; \[ ~ \] é apenas um valor.

Se name for prefixado com +, \[ ~ \] não deverá ser usado na coluna Value. Isso ocorre porque o significado de "+" e " \[ ~ \] " são claramente exclusivos um do outro.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de componentes](component-table.md). Esta coluna faz referência ao componente que controla a instalação dos valores de ambiente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para o instalador definir variáveis de ambiente, a ação [WriteEnvironmentStrings](writeenvironmentstrings-action.md) e a [ação RemoveEnvironmentStrings](removeenvironmentstrings-action.md) precisam ser listadas na [tabela InstallExecuteSequence](installexecutesequence-table.md).

Observe que as variáveis de ambiente não são alteradas para a instalação em andamento quando a ação [WriteEnvironmentStrings](writeenvironmentstrings-action.md) ou a [ação RemoveEnvironmentStrings](removeenvironmentstrings-action.md) são executadas. no Windows 2000, essas informações são armazenadas no registro e uma mensagem notifica o sistema sobre as alterações quando a instalação é concluída. Um novo processo ou outro processo que verifica essas mensagens usa as novas variáveis de ambiente.

Ao modificar a variável de ambiente Path com a tabela de ambiente, não tente inserir o novo caminho inteiro explicitamente no campo valor. Em vez disso, estenda o caminho existente prefixando ou anexando um valor e delimitador (;) para o \[ ~ \] . Se \[ ~ \] não estiver presente no campo valor, as informações de caminho existentes serão perdidas e a instalação do arquivo de .msi poderá impedir que o computador seja inicializado. A variável path é geralmente definida usando a sintaxe: \[ ~ \] ; Valor.

Ao executar instalações por máquina de um servidor de terminal, o instalador grava variáveis de ambiente por usuário para **HKU \\ . \\Ambiente padrão**. Como os serviços de terminal não replicam esta seção do registro, a instalação não define as variáveis de ambiente por usuário. Um pacote usado para instalações por máquina deve gravar variáveis de ambiente no ambiente do computador, incluindo \* na coluna nome. Se o pacote puder ser instalado por usuário ou por computador, crie dois componentes: (1) um componente por usuário com as entradas da tabela de ambiente criadas para as configurações do usuário e (2) um componente por máquina com a tabela de ambiente criada para as configurações do computador. Condição a instalação deste componente usando a propriedade [**Privileged**](privileged.md) .

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




