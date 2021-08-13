---
title: Compilador de mensagem (MC.exe)
description: Usado para compilar manifestos de instrumentação e arquivos de texto de mensagem.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Log de mensagens (MC.exe) EventLog
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470936"
---
# <a name="message-compiler-mcexe"></a>Compilador de mensagem (MC.exe)

Usado para compilar manifestos de instrumentação e arquivos de texto de mensagem. O compilador gera os arquivos de recurso de mensagem para os quais seu aplicativo se vincula.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argumentos comuns a arquivos de texto de mensagem e arquivos de manifesto](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Argumentos específicos para arquivos de manifesto](#arguments-specific-to-manifest-files)
-   [Argumentos específicos para gerar código que seu provedor usaria para registrar eventos](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argumentos específicos para arquivos de texto de mensagem](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argumentos comuns a arquivos de texto de mensagem e arquivos de manifesto

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Exibe as informações de uso para o compilador de mensagem.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Use este argumento para fazer com que o compilador defina o bit do cliente (bit 28) em todas as IDs de mensagem. Para obter informações sobre o bit do cliente, consulte Winerror. h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-CP** *Encoding*
</dt> <dd>

Use este argumento para especificar a codificação de caracteres usada para todos os arquivos de texto gerados. Os nomes válidos incluem "ANSI" (padrão), "UTF-8" e "UTF-16". As codificações Unicode adicionarão uma marca de ordem de byte.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extensão* **-e**
</dt> <dd>

Use este argumento para especificar a extensão a ser usada para o arquivo de cabeçalho. Você pode especificar até uma extensão de três caracteres, não incluindo o período. O padrão é. h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *caminho*
</dt> <dd>

Use este argumento para especificar a pasta na qual você deseja que o compilador Coloque o arquivo de cabeçalho gerado. O padrão é o diretório atual.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *comprimento*
</dt> <dd>

Use este argumento para que o compilador gere um aviso se a mensagem exceder caracteres de *comprimento* .

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *caminho*
</dt> <dd>

Use este argumento para especificar a pasta na qual você deseja que o compilador Coloque o script do compilador de recurso gerado (arquivo. rc) e os arquivos. bin gerados (recursos binários) que o script do compilador de recurso inclui. O padrão é o diretório atual.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nome*
</dt> <dd>

Use este argumento para substituir o nome de base padrão que o compilador usa para os arquivos que ele gera. O padrão é usar o nome de base do arquivo de entrada *filename* .

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

O arquivo de manifesto de instrumentação ou o arquivo de texto de mensagem. O arquivo deve existir no diretório atual. Você pode especificar um arquivo de manifesto, um arquivo de texto de mensagem ou ambos. O nome do arquivo deve incluir a extensão. A Convenção é usar uma extensão. Man para arquivos de manifesto e uma extensão. MC para arquivos de texto de mensagem.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Argumentos específicos para arquivos de manifesto

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s** *caminho*
</dt> <dd>

Use este argumento para criar uma linha de base de sua instrumentação. Especifique o caminho para a pasta que contém os arquivos de manifesto de linha de base. Para versões subsequentes, você usará o argumento **-t** para verificar o novo manifesto em relação à linha de base para problemas de compatibilidade.

**Antes do MC versão 1.12.7051:** Não disponível

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *caminho*
</dt> <dd>

Use esse argumento quando você criar uma nova versão do seu manifesto e quiser verificá-la para compatibilidade de aplicativos em relação à linha de base que você criou usando o argumento **-s** . O caminho deve apontar para a pasta que contém o. Arquivos BIN que a operação de linha de base criou (consulte a opção **-s** ).

**Antes do MC versão 1.12.7051:** Não disponível

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *caminho*
</dt> <dd>

O compilador ignora esse argumento e valida automaticamente o manifesto.

**Antes do MC versão 1.12.7051:** Use este argumento para especificar a pasta que contém o arquivo de esquema eventer. xsd, que o compilador usa para validar seu manifesto. a SDK do Windows inclui o arquivo de esquema eventer. xsd na \\ pasta Include. Se você não especificar esse argumento, o compilador não validará seu manifesto.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *caminho*
</dt> <dd>

O compilador ignora esse argumento.

**Antes do MC versão 1.12.7051:** Use este argumento para especificar a pasta que contém o arquivo de Winmeta.xml. O arquivo de Winmeta.xml contém os tipos de entrada e saída reconhecidos, bem como os canais, níveis e opcodes predefinidos. a SDK do Windows inclui o arquivo de Winmeta.xml na \\ pasta Include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argumentos específicos para gerar código que seu provedor usaria para registrar eventos

Você pode usar os seguintes argumentos do compilador para gerar o código do modo kernel ou do modo de usuário que você pode usar para registrar eventos. você também pode solicitar que o compilador gere código para dar suporte à gravação de eventos em computadores anteriores ao Windows Vista. Se seu aplicativo for escrito em C#, o compilador poderá gerar uma classe C# que você pode usar para registrar eventos. esses argumentos estão disponíveis a partir do MC versão 1.12.7051 que acompanha a versão Windows 7 do SDK do windows.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-co**
</dt> <dd>

Use este argumento para fazer com que o serviço de log chame sua função definida pelo usuário para cada evento que você registrar (a função é chamada após o registro do evento). Sua função definida pelo usuário deve ter a assinatura a seguir.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



Você também deve incluir a diretiva a seguir em seu código.

`#define MCGEN_CALLOUT pFnUserFunction`

Você deve manter sua implementação o mais curta possível para evitar problemas de log; o serviço não registrará mais os eventos até que a função seja retornada.

Você pode usar esse argumento com o argumento **-km** ou **-um** .

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*
</dt> <dd>

Use este argumento para que o compilador gere uma classe C# com base na classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-namespace de CSS** 
</dt> <dd>

Use este argumento para que o compilador gere uma classe C# estática com base na classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Use este argumento para que o compilador gere o código do modo kernel que você usaria para registrar os eventos definidos em seu manifesto.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-MOF**
</dt> <dd>

Preterido. use este argumento para que o compilador gere código que você pode usar para registrar eventos em computadores anteriores ao Windows Vista. Essa opção também cria um arquivo MOF que contém as classes MOF para cada evento definido no manifesto. Para registrar as classes no arquivo MOF para que os consumidores possam decodificar os eventos, use o compilador MOF (Mofcomp.exe). Para obter detalhes sobre como usar o compilador MOF, consulte [formato MOF](/windows/desktop/WmiSdk/managed-object-format--mof-).

Para usar essa opção, você deve aderir às seguintes restrições:

-   Cada definição de evento deve incluir a tarefa e os atributos de opcode
-   Cada tarefa deve incluir o atributo eventGuid
-   Os dados do modelo que as referências do evento não podem conter:
    -   Itens de dados que especificam os tipos de entrada Win: binary ou Win: SYSTEMTIME
    -   Estruturas
    -   Matrizes de tamanho variável; no entanto, você pode especificar matrizes de comprimento fixo
    -   Tipos de dados de cadeia de caracteres não podem especificar o atributo de comprimento

Você deve usar esse argumento com o argumento **-um**, **-cs**, **-CSS** ou **-km**

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefixo*
</dt> <dd>

Use este argumento para substituir o prefixo padrão que o compilador usa para os nomes de macro e nomes de método de registro em log. O prefixo padrão é "EventWrite". A cadeia de caracteres diferencia maiúsculas de minúsculas.

Você pode usar esse argumento com o argumento **-um**, **-cs**, **-CSS** ou **-km** .

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefixo*
</dt> <dd>

Use este argumento para remover os caracteres do início do nome simbólico que você especificou para o evento. A comparação não diferencia maiúsculas de minúsculas. O compilador usa o nome simbólico para formar os nomes de macro de log e nomes de método.

O nome padrão para uma macro de log é EventWrite *SymbolName,* em que *SymbolName* é o nome simbólico especificado para o evento. Por exemplo, se você definir o atributo de símbolo do evento como PrinterConnection, o nome da macro será EventWritePrinterConnection. Para remover a Impressora do nome, use **-P** **Printer**, que resulta em EventWriteConnection.

Você pode usar esse argumento com **o argumento -um**, **-cs**, **-css** ou **-km.**

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Use esse argumento para que o compilador gere o código de modo de usuário que você usaria para registrar os eventos definidos em seu manifesto.

</dd> </dl>

Para que o compilador gere o código de log, você deve especificar o **argumento -um**, **-cs**, **-css** ou **-km;** esses argumentos são mutuamente exclusivos.

Para especificar onde colocar os arquivos .h, .cs e .mof que o compilador gera, use o **argumento -h.** Se você não especificar o **argumento -h,** os arquivos serão colocados na pasta atual.

Para especificar onde colocar o arquivo .rc e os arquivos binários (que contêm os recursos de metadados) gerados pelo compilador, use o **argumento -r.** Se você não especificar o **argumento -r,** os arquivos serão colocados na pasta atual.

O compilador usa o nome base do arquivo de entrada como o nome base dos arquivos que ele gera. Para especificar um nome base, use o **argumento -z.**

### <a name="arguments-specific-to-message-text-files"></a>Argumentos específicos para arquivos de texto de mensagem

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Use esse argumento para especificar que o arquivo de entrada *filename* contém conteúdo na página de código ANSI Windows padrão do sistema (CP_ACP). Esse é o padrão. Use **-u** para Unicode. Se o arquivo de entrada contiver uma BOM, esse argumento será ignorado.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Preterido. Use esse argumento para especificar que as mensagens no arquivo .bin de saída devem ser ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Use esse argumento para que o compilador use o nome base do arquivo de entrada *filename* para os nomes de arquivo .bin. O padrão é usar "MSG".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Use esse argumento para usar valores decimais para as constantes Severity e Facility no arquivo de header em vez de valores hexadecimais.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Use esse argumento para especificar que as mensagens terminem imediatamente após o corpo da mensagem. O padrão é encerrar o corpo da mensagem com um CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Use esse argumento para que o compilador gere um arquivo de header OLE2 usando **definições HRESULT** em vez de códigos de status. Usar códigos de status é o padrão.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Use esse argumento para especificar que o *arquivo de entrada de nome* de arquivo contém conteúdo UTF-16LE. O padrão é o conteúdo ANSI. Se o arquivo de entrada contiver uma BOM, esse argumento será ignorado.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Use esse argumento para especificar que as mensagens no arquivo .bin de saída devem ser Unicode. Esse é o padrão.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Use esse argumento para gerar uma saída detalhada.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**Caminho -x** 
</dt> <dd>

Use esse argumento para especificar a pasta na qual você deseja que o compilador coloque o arquivo de inclusão .dbg C. O arquivo .dbg mapeia IDs de mensagem para seus nomes simbólicos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os **argumentos -A** e **-mof** foram preterido e serão removidos no futuro.

O compilador aceita como entrada um arquivo de manifesto (.man) ou um arquivo de texto de mensagem (.mc) e gera os seguintes arquivos:

-   *filename*.h

    Um arquivo de header C/C++ que contém os descritores de evento, o GUID do provedor e os nomes de símbolo que você referencia em seu aplicativo.

-   *filename* TEMP.bin

    Um arquivo de recurso binário que contém os metadados do provedor e do evento. Esse é o recurso de modelo, que é significado pelo sufixo TEMP do nome base do arquivo.

-   Msg00001.bin

    Um arquivo de recurso binário para cada idioma especificado (por exemplo, se o manifesto contiver cadeias de caracteres de mensagem em en-US e fr-FR, o compilador gerará Msg00001.bin e Msg00002.bin).

-   *filename*.rc

    Um script do compilador de recursos que contém as instruções para incluir cada arquivo .bin como um recurso.

Para argumentos que levam um caminho, o caminho pode ser um caminho absoluto, relativo ou UNC e pode conter variáveis de ambiente.

**Antes do MC versão 1.12.7051:** O compilador não permite caminhos relativos ou variáveis de ambiente.

O Windows SDK inclui o compilador (mc.exe) na \\ pasta Bin.

## <a name="examples"></a>Exemplos

O exemplo a seguir compila um manifesto usando os padrões do compilador.

``` syntax
mc spooler.man
```

O exemplo a seguir compila o manifesto e coloca o header e os arquivos de recurso nas pastas especificadas.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------------|
| Cliente mínimo com suporte | Windows 2000 Professional \[somente aplicativos da área de trabalho\] |
| Servidor mínimo com suporte | Windows 2000 Server \[somente aplicativos da área de trabalho\]       |
