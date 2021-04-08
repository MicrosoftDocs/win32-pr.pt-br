---
description: O compilador formato MOF (MOF) analisa um arquivo que contém instruções MOF e adiciona as classes e instâncias de classe definidas no arquivo ao repositório do WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: Mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827492"
---
# <a name="mofcomp"></a>Mofcomp

O compilador [*formato MOF (MOF)*](gloss-m.md) analisa um arquivo que contém instruções MOF e adiciona as classes e instâncias de classe definidas no arquivo ao repositório do WMI. Os arquivos MOF geralmente são compilados automaticamente durante a instalação dos sistemas com os quais eles são fornecidos, mas você também pode compilar arquivos MOF usando essa ferramenta.

Para obter mais informações sobre como localizar e usar mofcomp.exe, consulte [usando as ferramentas de gerenciamento do WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .

O exemplo de código a seguir mostra como executar o compilador MOF em um arquivo.

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>Comutadores

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-recuperação automática**
</dt> <dd>

Adiciona o arquivo MOF nomeado à lista de arquivos compilados durante a recuperação do repositório. A lista de arquivos MOF de recuperação automática é armazenada na chave do registro:

**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

Os arquivos MOF listados nesta entrada de registro devem residir no computador local porque os arquivos MOF que usam o comando de **recuperação automática** não podem recuperar arquivos MOF localizados em um computador remoto.

> [!Note]  
> Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e reiniciar, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo [*formato MOF*](gloss-m.md) (MOF).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-verificar**
</dt> <dd>

Solicita que o compilador execute apenas uma verificação de sintaxe e imprima as mensagens de erro apropriadas. Nenhuma outra opção pode ser usada com essa opção. Quando essa opção é usada, nenhuma conexão com Instrumentação de Gerenciamento do Windows (WMI) é estabelecida e nenhuma modificação no repositório do WMI é feita.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _NamespacePath_*_>_*
</dt> <dd>Solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*. O MOF compilado é carregado no namespace Mofcomp padrão, o \\ padrão raiz, a menos que essa opção seja usada. Você também pode inserir o namespace pragma do comando de pré-processador **\# ("**_caminho do namespace_*_")_* no arquivo MOF para obter o mesmo efeito. Se os comandos **-N:** switch e o \# <a href="pragma-namespace.md">namespace pragma</a> forem usados, o \# **namespace de pragma** **Recover** terá prioridade. Nesse caso, a única maneira de compilar o MOF em outro namespace é editar o arquivo MOF e alterar o comando de \# **namespace de pragma** . Um computador remoto pode ser especificado usando o \\ \\ \\ padrão raiz MachineName \\ .</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Class: somente**
</dt> <dd>

Solicita que o compilador não faça nenhuma alteração nas classes existentes. Quando essa opção for usada, a operação de compilação será encerrada se uma classe especificada no arquivo MOF já existir.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-classe: forceupdate**
</dt> <dd>

Força atualizações de classes quando existem classes filhas conflitantes. Por exemplo, suponha que um qualificador de classe seja definido em uma classe filho e a classe base tente adicionar o mesmo qualificador. Na **classe: modo forceupdate** , o compilador MOF resolve esse conflito excluindo o qualificador conflitante na classe filho. Se a classe filho tiver instâncias, a atualização forçada falhará.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-classe: safeupdate**
</dt> <dd>

Permite atualizações de classes, mesmo se houver classes filhas, desde que a alteração não cause conflitos com classes filhas. Por exemplo, esse sinalizador permite adicionar uma nova propriedade à classe base que não foi mencionada anteriormente em classes filhas. Se as classes filhas tiverem instâncias, a atualização falhará.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-classe: UpdateOnly**
</dt> <dd>

Solicita que o compilador não crie nenhuma classe nova. Quando essa opção for usada, a operação de compilação será encerrada se uma classe especificada no arquivo MOF não existir.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instância: UpdateOnly**
</dt> <dd>

Solicita que o compilador não crie nenhuma nova instância. Quando essa opção for usada, a operação de compilação será encerrada se uma instância especificada no arquivo MOF não existir.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instância: somente**
</dt> <dd>

Solicita que o compilador não faça nenhuma alteração nas instâncias existentes. Quando essa opção for usada, a operação de compilação será encerrada se uma instância especificada no arquivo MOF já existir.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _nome do arquivo_*_>_*
</dt> <dd>

Solicita que o compilador crie uma versão binária do arquivo MOF com o nome *nome* de arquivo sem fazer nenhuma modificação no repositório WMI.

Se você usar a opção **-B: <** _filename_ *_>_* para criar um arquivo MOF binário, somente os tipos de qualificador padrão serão armazenados no repositório WMI.

O formato binário MOF é o formato intermediário para combinar um driver WDM com o MOF como um recurso. O MOF binário representa classes e instâncias da mesma forma que um arquivo MOF de texto e é compactado antes de ser armazenado em disco.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Solicita que o compilador execute uma verificação de sintaxe do WMI. A opção **-B:** deve ser usada com essa opção. A opção **-WMI** é usada somente para criar arquivos MOF binários para uso por drivers de dispositivo WDM. Essa opção invoca um verificador de arquivo MOF binário separado, que é executado depois que o arquivo MOF binário é criado.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _senha_*_>_*
</dt> <dd>

Especifica a *senha* como a senha do usuário do computador a ser inserida ao fazer logon.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _nome de usuário_*_>_*
</dt> <dd>

Especifica *username* como o nome do usuário que está fazendo logon.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: autoridade de <** *_>_*
</dt> <dd>

Especifica a *autoridade* como a autoridade (nome de domínio) a ser usada ao fazer logon no WMI.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: caminho de <** *_>_*
</dt> <dd>

Nome da saída de idioma neutro. Usado com a opção **-aditamento** para especificar o nome do arquivo MOF com neutralidade de idioma que será gerado.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: caminho de <** *_>_*
</dt> <dd>

Nome da saída específica do idioma. Usado com a opção **-aditamento** para especificar o nome do arquivo MOF específico do idioma que será gerado.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Emenda: <** _localidade_*_>_*
</dt> <dd>

Divide o arquivo MOF em versões específicas de idioma e neutras. O compilador MOF cria uma forma neutra de idioma do arquivo MOF que tem todos os qualificadores corrigidos removidos. Uma versão localizada do arquivo MOF também é criada com uma extensão de nome de arquivo MFL. O parâmetro *locale* especifica o nome do namespace filho que contém as definições de classe localizadas. O formato do parâmetro *locale* é MS \_ xxx, em que xxx é o valor hexadecimal do LCID do Windows. Por exemplo, a localidade para inglês americano é MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*
</dt> <dd>

Extrai o MOF binário de um recurso nomeado. Essa opção Obtém o MOF binário da classe no repositório WMI, enquanto a opção-B cria o formato binário MOF a partir de um arquivo MOF.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*
</dt> <dd>

Opcional. Extrai as descrições do MOF localizadas do MOF binário quando usadas com a opção-ER.

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

Nome do arquivo a ser analisado.

</dd> </dl>

## <a name="return-values"></a>Valores de retorno

Como sua primeira operação, o compilador MOF executa uma verificação de sintaxe no arquivo MOF. Se o compilador encontrar erros, ele imprime uma mensagem de erro e o processo é encerrado.

O compilador MOF pode retornar os seguintes valores:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

A operação de compilação do MOF foi bem-sucedida.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

O compilador MOF não pôde se conectar ao servidor WMI. Isso ocorre devido a um erro semântico, como uma incompatibilidade com o repositório WMI existente ou um erro real, como a falha do servidor WMI para iniciar.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Uma ou mais opções de linha de comando não eram válidas.

</dd> <dt>

<span id="3"></span>Beta
</dt> <dd>

Ocorreu um erro de sintaxe do MOF.

</dd> </dl>

Se o arquivo MOF for analisado corretamente, mas for feita uma tentativa de executar uma operação proibida por uma opção de linha de comando, o compilador retornará um código de erro gerado pelo WMI em vez de qualquer um dos códigos de retorno listados na lista anterior. Por exemplo, um código de erro WMI é retornado quando a opção **-Instance: UpdateOnly** é especificada e o arquivo MOF tenta criar uma instância.

Se a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) não estiver no arquivo, o seguinte aviso será retornado:

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Comentários

O compilador MOF está disponível no diretório% windir% \\ System32 \\ WBEM. Você deve especificar o arquivo MOF como o parâmetro do compilador MOF. Você também pode especificar uma opção de recuperação automática se quiser que o arquivo MOF seja recompilado automaticamente se o repositório CIM precisar ser recuperado automaticamente. Para obter mais informações, digite **Mofcomp/?** no prompt de comando.

Um arquivo MOF que usa o conjunto de caracteres Unicode contém uma assinatura como os dois primeiros bytes do arquivo. Essa assinatura é U + FFFE ou U + FEFF, dependendo da ordenação de bytes do arquivo.

Quando nenhum erro ocorre no processo de análise, o compilador MOF se conecta ao servidor WMI em execução no computador local, a menos que a opção **-check** seja especificada. As classes e instâncias definidas no arquivo MOF são adicionadas ao repositório do WMI.

Quando ocorre um erro na atualização do repositório WMI, o compilador não faz nenhuma tentativa de retornar o repositório para seu estado antes do início do compilador.

**Windows 8:** Ao instalar um provedor, Mofcomp trata os \[ \] qualificadores de chave e \[ estático \] como true se estiverem presentes, independentemente de seus valores reais. Outros qualificadores são tratados como false se estiverem presentes, mas não definidos explicitamente como true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**namespace de pragma**](pragma-namespace.md)
</dt> <dt>

[Compilando arquivos MOF](compiling-mof-files.md)
</dt> <dt>

[Compilando arquivos MOF localizados](compiling-localized-mof-files.md)
</dt> <dt>

[Registrando um provedor](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler:: comcompilefile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

