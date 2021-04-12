---
description: A ferramenta CTRPP é um pré-processador que analisa e valida o manifesto de contadores.
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce12de641dda7b07871a4447190772533598748
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298020"
---
# <a name="ctrpp"></a>CTRPP

A ferramenta CTRPP é um pré-processador que analisa e valida o manifesto para seu provedor v2. A ferramenta gera `.rc` recursos com as cadeias de caracteres necessárias aos consumidores do seu provedor e gera um `.h` cabeçalho com o código que você usa para fornecer os dados do contador. Você deve executar a ferramenta CTRPP durante a compilação do seu provedor. Você deve usar o código gerado como um ponto de partida ao desenvolver seu provedor em vez de tentar gerar esse código por conta própria.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumentos

|Opção              |Descrição
|--------------------|-----------
|*inputFile*         |**Necessário:** Especifica o nome do `.man` arquivo (manifesto XML) que define seus contadores.
|**-o** *CodeFile*   |**Necessário:** Especifica o nome do `.h` arquivo de código a ser gerado pelo ctrpp. Esse arquivo conterá funções auxiliares embutidas em C/C++ que simplificam a inicialização e a desinicialização do seu provedor.
|**-RC** *rcFile*    |**Necessário:** Especifica o nome do `.rc` (arquivo de recurso) a ser gerado pelo ctrpp. Esse arquivo conterá a tabela de cadeias de caracteres do provedor.
|**-ch** *symFile*   |Especifica o nome do arquivo de `.h` símbolo opcional a ser gerado pelo ctrpp. Esse arquivo conterá símbolos C/C++ para os nomes e GUIDs de cada CounterSet no provedor.
|**-** *prefixo prefixo*|Especifica o prefixo a ser usado para as variáveis e funções definidas no arquivo de cabeçalho gerado.
|**-NotificationCallback**|Altera a assinatura padrão da função de [**Metainicialização**](counterinitialize.md) para incluir parâmetros para especificar o nome das funções de retorno de chamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest), [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)e [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Esse argumento tem o mesmo efeito que incluir o `callback` atributo no elemento [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) .
|**-migrar** *arquivo_de_saída*|Em vez de gerar `.h` e `.rc` arquivos, o atualiza o manifesto do arquivo de *entrada* para a versão mais recente e salva-o no arquivo de *saída*. Essa opção não pode ser usada com outras opções. Uso: `CTRPP -migrate NewFile.man OldFile.man`
|**-Compatibilidade de leitura**     |**Preterido:** O suporte para provedores de modo kernel foi adicionado ao Windows 7. Por padrão, o código gerado por CTRPP para provedores de modo kernel será incompatível com versões anteriores do Windows (haverá falha no carregamento do driver devido a APIs ausentes `Pcw***` ). Defina `-BackCompat` para habilitar a compatibilidade com versões anteriores do Windows. O driver carregará dinamicamente as APIs necessárias e o código gerado irá desabilitar o provedor silenciosamente se as APIs não estiverem disponíveis.
|**-MemoryRoutines** |**Preterido:** Quando usado com a `-Legacy` opção, inclui modelos para rotinas de memória no código gerado. Caso contrário, esse argumento terá o mesmo efeito que a `-NotificationCallback` opção.
|**-Herdado**         |**Preterido:** Gera `*.h` `*.c` arquivos,, e `*.rc` `*_r.h` usando os modelos de código do Windows Vista (gera PerfAutoInitialize e PerfAutoCleanup em vez de proinitialize e nocleanup). Essa opção pode ser usada com **-MemoryRoutines** e **-NotificationCallback** , mas não pode ser usada com outras opções. Não use os comutadores **-o** ou **-RC** com essa opção. Os arquivos gerados serão nomeados com base no nome do manifesto e serão gravados no diretório que continha o manifesto. Uso: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Comentários

A ferramenta CTRPP gera um arquivo de `.h` código, um `.rc` arquivo de recurso e, opcionalmente, gera um `.h` arquivo de símbolo.

### <a name="using-the-generated-resource-file"></a>Usando o arquivo de recursos gerado

A ferramenta CTRPP gerará um `.rc` arquivo de recurso que contém as cadeias de caracteres localizáveis necessárias aos consumidores dos conjuntos de linhas do provedor.

> [!IMPORTANT]
> Os recursos desse arquivo devem ser incluídos no seu binário do provedor e o caminho completo para o binário do provedor deve ser registrado durante a instalação do manifesto do provedor. Os consumidores que não puderem localizar e carregar os recursos não poderão usar os conjuntos de linhas do provedor.

Os recursos de cadeia de caracteres devem ser tratados da seguinte maneira:

- O desenvolvedor edita o arquivo de manifesto do provedor ( `.man` ) para definir o `applicationIdentity` atributo do provedor como o nome de um binário do provedor (. DLL,. SYS ou. EXE) que conterá os recursos de cadeia de caracteres para o provedor e será instalado como parte do componente do provedor.
- A ferramenta CTRPP lê o manifesto do provedor e gera um `.rc` arquivo.
- A ferramenta [RC (compilador de recurso)](../menurc/resource-compiler.md) compila os dados do arquivo gerado pelo ctrpp `.rc` para gerar um `.res` arquivo que contém os recursos binários. Isso pode ser feito por meio da compilação direta do arquivo gerado pelo CTRPP `.rc` ou pela compilação de outro `.rc` arquivo que inclui o `.rc` arquivo gerado por ctrpp por meio de uma `#include` diretiva.
- O vinculador incorpora os dados do arquivo gerado por RC `.res` para o binário do provedor.
- Durante a instalação, o binário do provedor é copiado no sistema do usuário e o manifesto do provedor é registrado usando a [ferramenta LodCtr](/windows-server/administration/windows-commands/lodctr). A ferramenta LodCtr converte o `applicationIdentity` atributo do manifesto do provedor em um caminho completo e registra o caminho completo para o binário do provedor no registro.
  - Se o binário do provedor estiver no mesmo diretório que o manifesto, use: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . Lodctr combinará o caminho de manifesto especificado com o atributo do manifesto `applicationIdentity` para formar o caminho completo.
  - Caso contrário, use `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. Lodctr combinará o caminho binário especificado com o atributo do manifesto `applicationIdentity` para formar o caminho completo.
  - Para fins de diagnóstico, você pode inspecionar o caminho completo gravado verificando o `ApplicationIdentity` valor da chave do registro `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Se o binário estiver usando o MUI para localização, certifique-se de copiar o arquivo MUI junto com o binário.
- Durante a coleta do CounterSet, o consumidor usa o caminho completo gravado para o binário do provedor para localizar e carregar as cadeias de caracteres necessárias dos recursos do binário do provedor.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Usando o arquivo de código gerado em um provedor de modo de usuário

A ferramenta CTRPP irá gerar um `.h` arquivo de código C/C++. Se o atributo do manifesto do provedor `providerType` for definido como `userMode` , o arquivo de código gerado conterá as seguintes definições que são úteis na codificação de um provedor de modo de usuário:

- Uma função de inicialização de provedor denominada [ * **prefix * preinitialize**](counterinitialize.md).
- Uma função de limpeza do provedor denominada [ * **prefix * procleanup**](countercleanup.md).
- Uma variável global ***Provider** _ que armazena o identificador do provedor aberto pela função _ *_prefix_CounterInitialize**. O nome da variável é o valor do `symbol` atributo do `provider` elemento no manifesto. Essa variável deve ser usada em chamadas para `PerfCreateInstance` , `PerfDeleteInstance` e outras APIs para controlar os dados do provedor.
- Para cada CounterSet, uma variável de **GUID global * CounterSet *** com o GUID do CounterSet. O nome da variável é o valor do `counterSet` atributo do elemento `symbol` mais o sufixo "GUID", por exemplo, `MyCounterSetGUID` . Essa variável deve ser usada em chamadas para `PerfCreateInstance` , `PerfDeleteInstance` e outras APIs para controlar os dados do provedor.
- Para cada contador, uma macro de ***contador*** com o valor do contador `id` . O nome da macro é o valor do `counter` atributo do elemento `symbol` . Essa macro deve ser usada em chamadas para `PerfSetCounterRefValue` , `PerfSetULongLongCounterValue` e outras APIs para definir os dados do provedor.

Nos nomes de função, ***prefix*** refere-se ao valor do `-prefix` parâmetro de linha de comando. Se o `-prefix` parâmetro não for usado, as funções serão nomeadas `CounterInitialize` e `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Usando o arquivo de código gerado em um provedor de modo kernel

A ferramenta CTRPP irá gerar um `.h` arquivo de código C/C++. Se o atributo do manifesto do provedor `providerType` for definido como `kernelMode` , o arquivo de código gerado conterá as seguintes definições que são úteis na codificação de conjuntos de valores de um provedor de modo kernel:

- Uma função de inicialização CounterSet denominada <b> *prefix* registrar *CounterSet*</b>. Essa função preenche uma estrutura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) , em seguida, invoca [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister), colocando o identificador de registro do CounterSet resultante na variável ***CounterSet*** global.
- Uma função de limpeza do CounterSet denominada <b> *prefix* cancelar registro do *CounterSet*</b>. Essa função invoca [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) no identificador de registro CounterSet na variável ***CounterSet*** global.
- Uma função de criação de instância denominada <b> *prefix* criar *CounterSet*</b>. Essa função preenche uma matriz de estruturas [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) , em seguida, invoca [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) usando o identificador de registro CounterSet na variável ***CounterSet*** global.
- Uma função de limpeza de instância denominada <b> *prefix* fechamento *CounterSet*</b>. Essa função invoca [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Uma função de relatório de instância chamada <b> *prefix* adiciona *CounterSet*</b> a ser usada na função de retorno de chamada CounterSet. Essa função preenche uma matriz de estruturas [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) e, em seguida, invoca [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **SDK do Windows 20H1 e posterior:** Uma função de inicialização RegInfo denominada <b> *prefix* InitRegistrationInformation *CounterSet*</b> para uso em cenários avançados. Essa função preenche uma estrutura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) . Essa função pode ser usada nos casos em que o <b>*contador* de registro de *prefixo*</b> gerado não atende às suas necessidades, por exemplo, quando você deseja personalizar os valores na estrutura RegInfo ou quando deseja armazenar o identificador retornado em outra variável.

Nos nomes de função, ***prefix*** refere-se ao valor do `-prefix` parâmetro de linha de comando. Se o `-prefix` parâmetro não for usado, as funções não terão nenhum prefixo.

> [!NOTE]
> O <b> *prefixo* gerado adicionar a função *CounterSet*</b> é usado quando você tem um retorno de chamada CounterSet. O <b> *prefixo* gerado criar *contadores*</b> e as funções <b>*CounterSet* de fechamento de *prefixo*</b> são usados quando você não tem um retorno de chamada CounterSet.

### <a name="using-the-generated-symbol-file"></a>Usando o arquivo de símbolo gerado

Se o parâmetro **-ch** for especificado na linha de comando, a ferramenta ctrpp irá gerar um `.h` arquivo de símbolo. Esse arquivo contém os símbolos C/C++ para os nomes e GUIDs de cada CounterSet no provedor. Os símbolos podem ser usados ao escrever programas que são embutidos em código para consumir os dados desse CounterSet usando as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisitos

|                         ||
|-------------------------|----
| Cliente mínimo com suporte| \[Somente aplicativos da área de trabalho do Windows Vista\]
| Servidor mínimo com suporte| \[Somente aplicativos da área de trabalho do Windows Server 2008\]
