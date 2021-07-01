---
description: A ferramenta CTRPP é um pré-processador que avalia e valida o manifesto dos contadores.
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
ms.openlocfilehash: eacfbb83abd56becc579c6b9bbaedacda96f94b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119101"
---
# <a name="ctrpp"></a>CTRPP

A ferramenta CTRPP é um pré-processador que avalia e valida o manifesto para seu provedor V2. A ferramenta gera recursos com as cadeias de caracteres necessárias para os consumidores do seu provedor e gera um header com o código que você usa para fornecer os dados `.rc` `.h` do contador. Você deve executar a ferramenta CTRPP durante o build do seu provedor. Você deve usar o código gerado como um ponto de partida ao desenvolver seu provedor em vez de tentar gerar esse código por conta própria.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumentos

|Opção              |Descrição
|--------------------|-----------
|*inputFile*         |**Obrigatório:** Especifica o nome do arquivo `.man` (manifesto XML) que define seus contadores.
|**-o** *codeFile*   |**Obrigatório:** Especifica o nome do arquivo `.h` de código a ser gerado pelo CTRPP. Esse arquivo conterá funções auxiliares em linha C/C++ que simplificam a inicialização e a não inicialização do provedor.
|**-rc** *rcFile*    |**Obrigatório:** Especifica o nome do `.rc` (arquivo de recurso) a ser gerado por CTRPP. Esse arquivo conterá a tabela de cadeia de caracteres do provedor.
|**-ch** *symFile*   |Especifica o nome do arquivo de símbolo opcional `.h` a ser gerado por CTRPP. Esse arquivo conterá símbolos C/C++ para os nomes e GUIDs de cada contador no provedor.
|**-prefixo de** *prefixo*|Especifica o prefixo a ser usado para as variáveis e funções definidas no arquivo de título gerado.
|**-NotificationCallback**|Altera a assinatura padrão da função [**CounterInitialize**](counterinitialize.md) para incluir parâmetros para especificar o nome das funções de retorno de chamada [*ControlCallback,*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)e [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Esse argumento tem o mesmo efeito que incluir o `callback` atributo no elemento [**do**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) provedor.
|**-migrar** *outputFile*|Em vez de gerar arquivos e , atualiza o manifesto inputFile para a versão mais recente e `.h` `.rc` salva-o em *outputFile*.  Essa opção não pode ser usada com outras opções. Uso: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**Preterido:** O suporte para provedores de modo kernel foi adicionado no Windows 7. Por padrão, o código gerado por CTRPP para provedores de modo kernel será incompatível com versões anteriores do Windows (o driver não será carregado devido a `Pcw***` APIs ausentes). Definido `-BackCompat` para habilitar a compatibilidade com versões anteriores do Windows. O driver carregará dinamicamente as APIs necessárias e o código gerado desabilitará silenciosamente o provedor se as APIs não estão disponíveis.
|**-MemoryRoutines** |**Preterido:** Quando usado com a `-Legacy` opção , inclui modelos para rotinas de memória no código gerado. Caso contrário, esse argumento terá o mesmo efeito que a `-NotificationCallback` opção .
|**-Legacy**         |**Preterido:** Gera arquivos , , e usando os modelos de código do `*.h` `*.c` Windows Vista `*.rc` `*_r.h` (gera PerfAutoInitialize e PerfAutoCleanup em vez de CounterInitialize e CounterCleanup). Essa opção pode ser usada com **-MemoryRoutines** e **-NotificationCallback,** mas não pode ser usada com nenhuma outra opção. Não use as opções **-o ou** **-rc** com essa opção. Os arquivos gerados serão nomeados com base no nome do manifesto e serão gravados no diretório que continha o manifesto. Uso: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Comentários

A ferramenta CTRPP gera um arquivo de código, um arquivo `.h` de recurso e, opcionalmente, gera um `.rc` arquivo de `.h` símbolo.

### <a name="using-the-generated-resource-file"></a>Usando o arquivo de recurso gerado

A ferramenta CTRPP gerará um arquivo de recurso que contém as cadeias de caracteres localizáveis necessárias para os consumidores dos contadores `.rc` do provedor.

> [!IMPORTANT]
> Os recursos desse arquivo devem ser incluídos no binário do provedor e o caminho completo para o binário do provedor deve ser registrado durante a instalação do manifesto do provedor. Os consumidores que não conseguem localizar e carregar os recursos não poderão usar os contadores do provedor.

Os recursos de cadeia de caracteres devem ser tratados da seguinte forma:

- O desenvolvedor edita o arquivo de manifesto do provedor ( ) para definir o atributo do provedor como o nome de um binário do provedor (.DLL, .SYS ou .EXE) que conterá os recursos de cadeia de caracteres para o provedor e será instalado como parte do componente do `.man` `applicationIdentity` provedor.
- A ferramenta CTRPP lê o manifesto do provedor e gera um `.rc` arquivo.
- A [ferramenta RC (compilador de recursos)](../menurc/resource-compiler.md) compila os dados do arquivo gerado por CTRPP para gerar um arquivo que contém `.rc` os recursos `.res` binários. Isso pode ser feito compilando diretamente o arquivo gerado por CTRPP OU compilando outro arquivo que inclui o arquivo gerado por `.rc` CTRPP por meio de `.rc` `.rc` uma diretiva `#include` .
- O vinculador inseri os dados do arquivo gerado pelo RC `.res` no binário do provedor.
- Durante a instalação, o binário do provedor é copiado para o sistema do usuário e o manifesto do provedor é registrado usando a [ferramenta lodctr](/windows-server/administration/windows-commands/lodctr). A ferramenta lodctr converte o atributo do manifesto do provedor em um caminho completo e registra o caminho completo para o binário do `applicationIdentity` provedor no Registro.
  - Se o binário do provedor estiver no mesmo diretório que o manifesto, use: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr combinará o caminho do manifesto especificado com o atributo do `applicationIdentity` manifesto para formar o caminho completo.
  - Caso contrário, use `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr combinará o caminho binário especificado com o atributo do `applicationIdentity` manifesto para formar o caminho completo.
  - Para fins de diagnóstico, você pode inspecionar o caminho completo gravado verificando o `ApplicationIdentity` valor da chave do Registro `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Se o binário estiver usando a MUI para localização, copie o arquivo MUI junto com o binário.
- Durante a coleta do conjunto de contadores, o consumidor usa o caminho completo registrado para o binário do provedor para localizar e carregar as cadeias de caracteres necessárias dos recursos do binário do provedor.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Usando o arquivo de código gerado em um provedor de modo de usuário

A ferramenta CTRPP gerará um `.h` arquivo de código C/C++. Se o atributo do manifesto do provedor for definido como , o arquivo de código gerado conterá as seguintes definições úteis na codificação de um `providerType` provedor de modo de `userMode` usuário:

- Uma função de inicialização de provedor chamada [ * **prefix*CounterInitialize.**](counterinitialize.md)
- Uma função de limpeza do provedor chamada [ * **prefix*CounterCleanup.**](countercleanup.md)
- Um provedor ***** global _ variável que armazena o handle do provedor aberto pela função _ *_prefix_CounterInitialize**. O nome da variável é o valor `symbol` do atributo do elemento no `provider` manifesto. Essa variável deve ser usada em chamadas para , e outras `PerfCreateInstance` `PerfDeleteInstance` APIs para controlar os dados do provedor.
- Para cada contador, uma variável global ***counterset*GUID** com o GUID do counterset. O nome da variável é o valor do atributo do elemento mais o `counterSet` `symbol` sufixo "GUID", por exemplo, `MyCounterSetGUID` . Essa variável deve ser usada em chamadas para , e outras `PerfCreateInstance` `PerfDeleteInstance` APIs para controlar os dados do provedor.
- Para cada contador, uma macro ***de*** contador com o valor do `id` contador. O nome da macro é o valor `counter` do atributo do `symbol` elemento. Essa macro deve ser usada em chamadas para , e outras `PerfSetCounterRefValue` `PerfSetULongLongCounterValue` APIs para definir os dados do provedor.

Nos nomes de função, ***prefixo*** refere-se ao valor do parâmetro `-prefix` de linha de comando. Se o `-prefix` parâmetro não for usado, as funções serão nomeadas `CounterInitialize` e `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Usando o arquivo de código gerado em um provedor de modo kernel

A ferramenta CTRPP gerará um `.h` arquivo de código C/C++. Se o atributo do manifesto do provedor for definido como , o arquivo de código gerado conterá as seguintes definições úteis para codificar os contadores de um provedor de modo `providerType` `kernelMode` kernel:

- Uma função de inicialização de conjuntos de contadores chamada <b> *prefixo* Register *Counterset*</b>. Essa função preenche uma estrutura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) e, em seguida, invoca [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister), colocando o alçamento de registro do counterset resultante na variável global ***Counterset.***
- Uma função de limpeza do counterset chamada <b> *prefix* Unregister *Counterset*</b>. Essa função invoca [PcwUnregister na alça](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) de registro do counterset na variável global ***Counterset.***
- Uma função de criação de instância chamada <b> *prefixo* Create *Counterset*</b>. Essa função preenche uma matriz de estruturas [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) e, em seguida, invoca [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) usando o alça de registro do conjunto de contadores na variável global ***Counterset.***
- Uma função de limpeza de instância chamada <b> *prefixo* Close *Counterset*</b>. Essa função invoca [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Uma função de relatório de instância chamada <b> *prefix* Add *Counterset*</b> a ser usada da função de retorno de chamada do counterset. Essa função preenche uma matriz de estruturas [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) e, em seguida, invoca [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **SDK do Windows 20H1 e posterior:** Uma função de inicialização RegInfo chamada <b> *prefix* InitRegistrationInformation *Counterset*</b> para uso em cenários avançados. Essa função preenche uma estrutura [RegInfo.](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) Essa função pode ser usada em casos em que o <b> *prefixo* gerado Registrar *Counterset*</b> não atender às suas necessidades, por exemplo, quando você deseja personalizar os valores na estrutura RegInfo ou quando você deseja armazenar o alça retornado em outra variável.

Nos nomes de função, ***prefixo*** refere-se ao valor do parâmetro `-prefix` de linha de comando. Se o `-prefix` parâmetro não for usado, as funções não terão prefixo.

> [!NOTE]
> A função <b>Add *Counterset do* *prefixo*</b> gerado é usada quando você tem um retorno de chamada de counterset. O <b> *prefixo* gerado criar *contadores*</b> e as funções <b>*CounterSet* de fechamento de *prefixo*</b> são usados quando você não tem um retorno de chamada CounterSet.

### <a name="using-the-generated-symbol-file"></a>Usando o arquivo de símbolo gerado

Se o parâmetro **-ch** for especificado na linha de comando, a ferramenta ctrpp irá gerar um `.h` arquivo de símbolo. Esse arquivo contém os símbolos C/C++ para os nomes e GUIDs de cada CounterSet no provedor. Os símbolos podem ser usados ao escrever programas que são embutidos em código para consumir os dados desse CounterSet usando as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisitos

| Requisito             | Valor |
|-------------------------|-------|
| Cliente mínimo com suporte| \[Somente aplicativos da área de trabalho do Windows Vista\]
| Servidor mínimo com suporte| \[Somente aplicativos da área de trabalho do Windows Server 2008\]
