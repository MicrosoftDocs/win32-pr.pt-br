---
description: O WMI disponibiliza dados sobre Windows gerenciáveis por meio de provedores WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Fornecendo dados ao WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22fbff46959c001f589587f21b8b2b50ab5c5187d387338f407bf45e3e1a29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316570"
---
# <a name="providing-data-to-wmi"></a>Fornecendo dados ao WMI

O WMI disponibiliza dados sobre Windows gerenciáveis por meio de [*provedores WMI*](gloss-p.md). Um provedor recupera dados de um componente do sistema, como um processo ou um aplicativo instrumentado, como SNMP ou IIS, e passa esses dados por meio do WMI para um aplicativo de gerenciamento. Por exemplo, quando um aplicativo ou script solicita informações de processo usando a classe WMI [**Win32 \_ Process,**](/windows/desktop/CIMWin32Prov/win32-process) os dados são obtidos dinamicamente por meio de um provedor pré-instalado.

As seções a seguir são discutidas neste tópico:

-   [Criando um modelo para um objeto gerenciável](#creating-a-model-for-a-manageable-object)
-   [Implementando um modelo para um objeto gerenciável](#implementing-a-model-for-a-manageable-object)
-   [Determinando um tipo de provedor a ser implementado](#determining-a-provider-type-to-implement)
-   [Determinando um modelo de hospedagem (implementação) para um provedor](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementando um provedor](#implementing-a-provider)
-   [Registrando um provedor com o WMI e o sistema](#registering-a-provider-with-wmi-and-the-system)
-   [Testando um provedor](#testing-a-provider)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Criando um modelo para um objeto gerenciável

Antes de desenvolver um provedor, crie um modelo de dados para representar o objeto gerenciável a ser exposto por meio do WMI. Você planeja quais objetos de dados seu provedor exporá. Por exemplo, se você planeja gerenciar a resolução de tela da tela de fundo da área de trabalho, deve decidir como modelar a Área de Trabalho em um arquivo [*MOF (Managed Object Format).*](gloss-m.md)

Para criar um modelo útil:

-   Determine cenários do mundo real e modele as informações que um cliente pode querer ler e atualizar (por exemplo, alterar a imagem de plano de fundo) para cada objeto gerenciável. Essas são suas propriedades de classe.
-   Determine quais tipos de ações um cliente pode querer executar com cada objeto gerenciável. Esses são seus métodos.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementando um modelo para um objeto gerenciável

Para implementar um modelo para objetos gerenciáveis, crie um arquivo MOF contendo uma classe WMI que representa cada objeto. Para obter mais informações sobre como criar um arquivo MOF para definir classes WMI, consulte [Criando classes Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md) O registro do provedor e suas classes geralmente são incluídos no arquivo MOF, embora seja possível usar a [API COM](com-api-for-wmi.md) para criar classes e métodos. Para obter mais informações, consulte [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

> [!Note]  
> Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas no repositório WMI se o [*WMI*](gloss-w.md) tiver uma falha e reiniciar, use a instrução de pré-processador de recuperação automática [**\# pragma**](pragma-autorecover.md) no arquivo [*MOF (Managed Object Format).*](gloss-m.md)

 

Depois de criar o arquivo MOF, compile-o usando a [**Mofcomp.exe**](mofcomp.md) de dados. Isso notifica você sobre erros no arquivo MOF e adiciona a classe WMI definida no arquivo MOF ao repositório [*WMI*](gloss-w.md) para que a classe possa ser usada por um provedor.

## <a name="determining-a-provider-type-to-implement"></a>Determinando um tipo de provedor a ser implementado

O WMI dá suporte a um determinado número de tipos de provedor, que determina a natureza das informações entregues e das operações compatíveis com os provedores.

Os tipos de provedor são:

-   [*Provedor de instância*](gloss-i.md)
-   [*Provedor de método*](gloss-m.md)
-   [*Provedor de propriedades*](gloss-p.md)
-   Provedor de classe
-   [*Provedor de eventos*](gloss-e.md)
-   [*Provedor de consumidor de eventos*](gloss-e.md)
-   [*Provedor de associação*](gloss-a.md)

A grande maioria dos provedores são provedores de instância e provedores de método. Um provedor de instância é o provedor mais comum e fornece as instâncias de uma determinada classe. Um provedor de métodos implementa os métodos de uma ou mais classes. Para obter mais informações sobre os tipos de provedores, consulte [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinando um modelo de hospedagem (implementação) para um provedor

Os provedores WMI são binários implementados como objetos COM. Isso significa que cada provedor tem um arquivo DLL que pode ser executado dentro de um processo específico e contexto de segurança. Isso é o que o WMI se refere como o modelo [*de hospedagem*](gloss-h.md). O WMI oferece várias maneiras de hospedar provedores, mas a abordagem mais comum é usar o modelo de provedor a par (em execução no processo WMI) no contexto de segurança NetworkServiceHost. Um provedor WMI pode ser classificado como apareado [*ou desacoplado.*](gloss-d.md)

O termo provedor a coupled ou desaplado determina sob qual processo de host o provedor está sendo executado em relação ao processo de WMIPRVSE.EXE WMI fornecido. Uma melhor prática é determinar se os dados de gerenciamento que o provedor expõe e a API ou o aplicativo do qual ele depende estão sempre disponíveis no sistema ou não. Se a API ou o aplicativo em que o provedor depende estiver sempre disponível (em execução no sistema), o provedor deverá ser um provedor a par, caso não seja, deve ser um provedor desaplado. Para obter mais informações sobre como hospedar modelos, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)

Para obter mais informações sobre como criar um provedor a coupled, consulte Fornecendo dados ao [WMI](supplying-data-to-wmi-by-writing-a-provider.md)escrevendo um provedor e para obter informações sobre como incorporar um provedor desaplados em um aplicativo, consulte [Incorporando](incorporating-a-provider-in-an-application.md)um provedor em um aplicativo .

Provedores a coupled podem ser descritos como em processo (em processo) ou fora do processo (fora do processo). Quando um provedor a coupled é um provedor in-proc, ele é executado em um processo de hospedagem de WMI de WMIPRVSE.EXE compartilhado e é implementado como um servidor in-proc COM (.dll). Quando um provedor é um provedor fora do processo, ele é iniciado pelo WMI na solicitação de um cliente ou evento, mas é executado como um processo separado e é implementado como um executável (.exe).

## <a name="implementing-a-provider"></a>Implementando um provedor

Um provedor pode ser implementado das seguintes maneiras:

-   Usando o Assistente atl em Visual Studio.

    O Assistente da ATL gera o código do provedor que implementa um provedor a coupled. Ao usar o Assistente atl, você pode especificar que deseja criar um modelo de tempo de run-time do provedor in-proc (.dll) ou fora do processo (.exe).

-   Definir um objeto COM para conter seu provedor.

    O código do provedor é escrito em C++. Para obter mais informações, [consulte Fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md).

-   Usando as classes no namespace [**Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) no .NET Framework para criar um provedor usando código gerenciado. (Não há mais suporte para o namespace **System.Management.Instrumentation.)**

    Esse processo cria um provedor desaplados.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrando um provedor com o WMI e o sistema

Antes de usar o provedor de um consumidor, é importante registrá-lo com o sistema WMI e o subsistema COM Windows com.

Um arquivo MOF pode conter vários tipos de provedores para as mesmas classes. O mesmo nome do provedor é registrado como, por exemplo, uma instância ou um provedor de método. Para obter mais informações, [consulte Registrando um provedor](registering-a-provider.md).

## <a name="testing-a-provider"></a>Testando um provedor

Quando o código do provedor é registrado, é importante testar corretamente o provedor usando o provedor de diferentes consumidores (por exemplo, scripts, código gerenciado .NET e consumidores C++).

Execute as seguintes tarefas para testar seu provedor:

-   Verifique se o provedor está carregando corretamente acompanhando as notificações de evento [**\_ MSFT WmiProvider \_ OperationEvent.**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) Esses eventos informarão sobre falhas de carga do provedor. Outras classes de solução de problemas que podem ser úteis [**são Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) e [**Win32 \_ ProcessStopTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) Para obter mais informações sobre como solucionar problemas de provedores, consulte [Depurando](debugging-providers.md) provedores e [configuração de](provider-configuration-and-troubleshooting-classes.md)provedor e classes de solução de problemas .
-   Se o provedor for uma instância ou um provedor de método, teste cada capacidade de provedor um por um para evitar confusão ao seguir sua lógica de código.
-   Para um provedor de instância, crie um aplicativo cliente ou script que invoca cada interface do provedor (enumeração, get, put e delete). Mesmo que o provedor não deva implementar nada, ele deverá retornar uma mensagem "sem suporte". Você pode encontrar os valores de retorno já definidos em [Códigos de Retorno WMI](wmi-return-codes.md).
-   Para garantir que o contexto de segurança desejado está funcionando como planejado, invoque as operações com suporte do provedor de um contexto de segurança nãoadministrador. O provedor deve dar suporte à representação. Se um usuário sem as credenciais de segurança corretas tentar atualizar dados ou executar uma operação que execute um método, o provedor deverá negar o acesso com a mensagem de erro apropriada.
-   Para obter mais informações sobre a segurança do provedor, consulte [Proteger seu provedor.](securing-your-provider.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedagem e segurança do provedor](provider-hosting-and-security.md)
</dt> <dt>

[Fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrando um provedor](registering-a-provider.md)
</dt> <dt>

[Solução de problemas de aplicativos cliente WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Proteger seu provedor](securing-your-provider.md)
</dt> <dt>

[Obter e fornecer dados em uma plataforma de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
