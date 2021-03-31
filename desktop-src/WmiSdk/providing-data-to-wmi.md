---
description: O WMI torna os dados sobre os objetos gerenciáveis do Windows disponíveis por meio de provedores WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Fornecendo dados ao WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647695"
---
# <a name="providing-data-to-wmi"></a>Fornecendo dados ao WMI

O WMI torna os dados sobre os objetos gerenciáveis do Windows disponíveis por meio de [*provedores*](gloss-p.md)WMI. Um provedor recupera dados de um componente do sistema, como um processo, ou um aplicativo instrumentado, como SNMP ou IIS, e passa esses dados por meio do WMI para um aplicativo de gerenciamento. Por exemplo, quando um aplicativo ou script solicita informações de processo usando a classe de [**\_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) , os dados são obtidos dinamicamente por meio de um provedor pré-instalado.

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

Antes de desenvolver um provedor, crie um modelo de dados para representar o objeto gerenciável a ser exposto por meio do WMI. Você planeja quais objetos de dados seu provedor vai expor. Por exemplo, se você planeja gerenciar a resolução de tela do plano de fundo da área de trabalho, você deve decidir como modelar a área de trabalho em um arquivo [*formato MOF (MOF)*](gloss-m.md) .

Para criar um modelo útil:

-   Determine cenários do mundo real e modele as informações que um cliente talvez queira ler e atualizar (por exemplo, alterar a imagem de plano de fundo) para cada objeto gerenciável. Essas são suas propriedades de classe.
-   Determine o tipo de ações que um cliente pode querer executar com cada objeto gerenciável. Esses são seus métodos.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementando um modelo para um objeto gerenciável

Para implementar um modelo para objetos gerenciáveis, crie um arquivo MOF contendo uma classe WMI que represente cada objeto. Para obter mais informações sobre como criar um arquivo MOF para definir classes WMI, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md). O registro do provedor e suas classes geralmente são incluídos no arquivo MOF, embora seja possível usar a [API com](com-api-for-wmi.md) para criar classes e métodos. Para obter mais informações, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

> [!Note]  
> Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e reiniciar, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo [*formato MOF (MOF)*](gloss-m.md) .

 

Depois de criar o arquivo MOF, compile-o usando a ferramenta [**Mofcomp.exe**](mofcomp.md) . Isso notifica você sobre erros no arquivo MOF e adiciona a classe WMI definida no arquivo MOF ao [*repositório WMI*](gloss-w.md) para que a classe possa ser usada por um provedor.

## <a name="determining-a-provider-type-to-implement"></a>Determinando um tipo de provedor a ser implementado

O WMI dá suporte a um determinado número de tipos de provedor, que determina a natureza das informações entregues e as operações com suporte dos provedores.

Os tipos de provedor são:

-   [*Provedor de instância*](gloss-i.md)
-   [*Provedor de método*](gloss-m.md)
-   [*Provedor de propriedades*](gloss-p.md)
-   Provedor de classe
-   [*Provedor de eventos*](gloss-e.md)
-   [*Provedor de consumidor de eventos*](gloss-e.md)
-   [*Provedor de associação*](gloss-a.md)

A grande maioria dos provedores são provedores de instâncias e provedores de métodos. Um provedor de instância é o provedor mais comum e fornece as instâncias de uma determinada classe. Um provedor de método implementa os métodos de uma ou mais classes. Para obter mais informações sobre os tipos de provedores, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinando um modelo de hospedagem (implementação) para um provedor

Provedores WMI são binários implementados como objetos COM. Isso significa que cada provedor tem um arquivo DLL que pode ser executado dentro de um processo e contexto de segurança específicos. Isso é o que o WMI se refere como o [*modelo de hospedagem*](gloss-h.md). O WMI oferece várias maneiras de hospedar provedores, mas a abordagem mais comum é usar o modelo de provedor acoplado (em execução no processo WMI) no contexto de segurança NetworkServiceHost. Um provedor WMI pode ser classificado como acoplado [*ou*](gloss-d.md)dissociado.

O termo de provedor acoplado ou dissociado determina sob qual processo de host o provedor está sendo executado em relação ao processo de WMIPRVSE.EXE fornecido pelo WMI. Uma prática recomendada é determinar se os dados de gerenciamento que o provedor expõe e a API ou o aplicativo do qual ele depende estão sempre disponíveis no sistema ou não. Se a API ou o aplicativo do qual o provedor depende estiver sempre disponível (em execução no sistema), o provedor deverá ser um provedor acoplado, caso contrário, deve ser um provedor desacoplado. Para obter mais informações sobre modelos de hospedagem, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

Para obter mais informações sobre como criar um provedor acoplado, consulte [fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md)e para obter informações sobre como incorporar um provedor dissociado em um aplicativo, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).

Provedores acoplados podem ser descritos como em processo (em processamento) ou fora de processo (fora do procedimento). Quando um provedor acoplado é um provedor em processo, ele é executado em um processo de hospedagem do WMI WMIPRVSE.EXE compartilhado e é implementado como um servidor no proc (. dll) COM. Quando um provedor é um provedor fora do processo, ele é iniciado pela WMI na solicitação de um cliente ou evento, mas é executado como um processo separado e é implementado como um executável (. exe).

## <a name="implementing-a-provider"></a>Implementando um provedor

Um provedor pode ser implementado das seguintes maneiras:

-   Usando o assistente de ATL no Visual Studio.

    O assistente do ATL gera o código do provedor que implementa um provedor acoplado. Ao usar o assistente ATL, você pode especificar que deseja criar um modelo de tempo de execução (. dll) ou fora do processo (. exe) no procedimento.

-   Definindo um objeto COM para conter seu provedor.

    O código do provedor é escrito em C++. Para obter mais informações, consulte [fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md).

-   Usando as classes no namespace [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) no .NET Framework para criar um provedor usando código gerenciado. (Não há mais suporte para o namespace **System. Management. Instrumentation** .)

    Esse processo cria um provedor dissociado.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrando um provedor com o WMI e o sistema

Antes de usar o provedor de um consumidor, é importante registrá-lo no sistema WMI e no subsistema COM do Windows.

Um arquivo MOF pode conter vários tipos de provedores para as mesmas classes. O mesmo nome de provedor é registrado como, por exemplo, uma instância ou um provedor de métodos. Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).

## <a name="testing-a-provider"></a>Testando um provedor

Quando o código do provedor é registrado, é importante testar corretamente o provedor usando o provedor de consumidores diferentes (por exemplo, scripts, código gerenciado do .NET e consumidores do C++).

Execute as seguintes tarefas para testar seu provedor:

-   Verifique se o provedor está carregando corretamente rastreando as notificações de evento do [**MSFT \_ WmiProvider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) . Esses eventos informarão sobre quaisquer falhas de carregamento do provedor. Outras classes de solução de problemas que podem ser úteis são [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) e [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace). Para obter mais informações sobre como solucionar problemas de provedores, consulte [Depurando provedores](debugging-providers.md) e [configuração de provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md).
-   Se o provedor for uma instância ou um provedor de métodos, certifique-se de testar cada recurso de provedor, um por um, para evitar confusão na seguinte lógica de código.
-   Para um provedor de instância, crie um aplicativo cliente ou script que invoca todas as interfaces do provedor (Enumeração, Get, PUT e Delete). Mesmo que o provedor não deva implementar nada, ele deve retornar uma mensagem "sem suporte". Você pode encontrar os valores de retorno já definidos nos [códigos de retorno do WMI](wmi-return-codes.md).
-   Para garantir que o contexto de segurança desejado esteja funcionando como planejado, invoque as operações com suporte do provedor de um contexto de segurança não administrador. O provedor deve dar suporte à representação. Se um usuário sem as credenciais de segurança corretas tentar atualizar dados ou executar uma operação que execute um método, seu provedor deverá negar o acesso com a mensagem de erro apropriada.
-   Para obter mais informações sobre a segurança do provedor, consulte [protegendo seu provedor](securing-your-provider.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedagem e segurança de provedor](provider-hosting-and-security.md)
</dt> <dt>

[Fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrando um provedor](registering-a-provider.md)
</dt> <dt>

[Solucionando problemas de aplicativos cliente WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> <dt>

[Obtenção e fornecimento de dados em uma plataforma de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
