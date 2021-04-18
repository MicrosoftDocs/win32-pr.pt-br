---
title: Glossário de Gerenciamento Remoto do Windows
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105789931"
---
# <a name="windows-remote-management-glossary"></a>Glossário de Gerenciamento Remoto do Windows


<dl> <dt>

WSMan: itens * * * *
</dt> <dd>

Um elemento de protocolo WS-Management retornado em uma enumeração que obtém as instâncias e a instância [*EPRS*](/windows). **WSMan: Items** é um contêiner que mantém uma instância e seu EPR. Esse tipo de enumeração é iniciado quando o sinalizador **WSManFlagReturnObjectAndEPR** é definido na solicitação.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**Baseboard Management Controller (BMC)**
</dt> <dd>

Um microcontrolador conectado localmente a um servidor. BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo que o servidor esteja offline. Você tem acesso aos dados do BMC por meio do provedor WMI da [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Autenticação básica**
</dt> <dd>

O nome de usuário e a senha enviados na troca de autenticação. A autenticação básica pode ser configurada para usar o transporte HTTP ou HTTPS em um domínio ou grupo de trabalho. Esse método é o método menos seguro de autenticação.

</dd> <dt>

**BMC**
</dt> <dd>

Consulte [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**CIM**
</dt> <dd>

Consulte [*modelo CIM (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**cliente**
</dt> <dd>

O aplicativo cliente que usa o protocolo WS-Management para acessar o serviço de gerenciamento no computador local ou remoto.

</dd> <dt>

**CIM (Modelo de Informação Comum)**
</dt> <dd>

O modelo [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) que descreve como representar objetos de rede e computador do mundo real. O CIM usa um paradigma orientado a objeto, em que os objetos gerenciados são modelados usando os conceitos de classes e instâncias.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticação Digest**
</dt> <dd>

Um Exchange em que o servidor recebe uma solicitação de um cliente e envia dados sobre o cliente para um servidor de autenticação, normalmente um controlador de domínio. Se o cliente for autenticado, o servidor receberá uma chave de sessão de resumo usada para autenticar solicitações subsequentes do cliente.

</dd> <dt>

**DMTF (Distributed Management Task Force)**
</dt> <dd>

A organização do setor que desenvolve os padrões de gerenciamento e a tecnologia de integração para ambientes corporativos e de Internet.

</dd> <dt>

**DMTF**
</dt> <dd>

Consulte [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Um recurso que pode ser resolvido por uma [*referência de ponto de extremidade (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**referência de ponto de extremidade (EPR)**
</dt> <dd>

Uma combinação de WS-Addressing e WS-Management elementos de endereçamento que descrevem em conjunto um endereço para um recurso no cabeçalho SOAP da mensagem. Este é um termo de serviço Web.

</dd> <dt>

**enumeração**
</dt> <dd>

Um conjunto, ou coleção, de instâncias de [*recurso*](windows-remote-management-glossary.md) ou a ação de solicitar um conjunto desse tipo. No protocolo WS-Management, o [*WS-Enumeration*](windows-remote-management-glossary.md) é usado para obter a coleção. Na implementação de script do serviço WinRM de enumeração, [**Session. enumerar**](session-enumerate.md) e o objeto [**Enumerator**](enumerator.md) são usados. O método e a interface C++ correspondentes são [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Consulte [*referência de ponto de extremidade (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Serviço de coleta de eventos**
</dt> <dd>

O componente do sistema operacional que recebe eventos do BMC e outros componentes ou aplicativos do sistema operacional.

</dd> <dt>

**encaminhamento de eventos**
</dt> <dd>

Uma notificação de eventos que ocorrem em computadores remotos pode ser enviada para aplicativos de assinatura. O encaminhamento de eventos não é um recurso do WinRM, mas do [log de eventos do Windows](/windows/desktop/WES/windows-event-log). O encaminhamento de eventos se torna disponível pela primeira vez no Windows Vista. Os aplicativos de gerenciamento, como o Microsoft Operations Manager (MOM), usam o encaminhamento de eventos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Um mecanismo de consulta para especificar um conjunto limitado de instâncias na solicitação de um [*recurso*](windows-remote-management-glossary.md). Você pode especificar um parâmetro de *filtro* em chamadas para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialeto do filtro**
</dt> <dd>

Uma cadeia de caracteres XML que identifica o dialeto XML usado para especificar um [*filtro*](windows-remote-management-glossary.md) em uma chamada para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). O serviço WinRM oferece suporte a [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como um dialeto de filtro ao receber solicitações.

</dd> <dt>

**fragmento**
</dt> <dd>

Uma cadeia de caracteres XML que identifica parte de uma instância de um recurso em vez de todo o recurso. Suporte a fragmento encontrado no objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**dialeto de fragmento**
</dt> <dd>

Uma cadeia de caracteres XML que identifica o dialeto XML usado para especificar um [*fragmento*](windows-remote-management-glossary.md). Suporte a fragmento encontrado no objeto [**ResourceLocator**](resourcelocator.md) . O serviço WinRM oferece suporte a [*XPath*](windows-remote-management-glossary.md) para dialeto de fragmento ao receber solicitações.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**em banda**
</dt> <dd>

O aplicativo cliente obtém dados do BMC por meio do [*ouvinte*](windows-remote-management-glossary.md) do WinRM no sistema operacional.

</dd> <dt>

**IPMI (interface de gerenciamento de plataforma inteligente)**
</dt> <dd>

Um padrão do setor de ti para a arquitetura do [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md). Os recursos de gerenciamento de hardware do Windows fornecem um [*driver IPMI*](windows-remote-management-glossary.md) e um [*provedor WMI IPMI*](windows-remote-management-glossary.md) que permite que scripts de gerenciamento, ferramentas de linha de comando e aplicativos obtenham dados do BMC. O provedor IPMI tem [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.

</dd> <dt>

**IPMI**
</dt> <dd>

Consulte [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md).

</dd> <dt>

**Driver IPMI**
</dt> <dd>

O driver de kernel que habilita o acesso a dispositivos [*BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) dos componentes do sistema operacional.

</dd> <dt>

**Provedor IPMI**
</dt> <dd>

Um provedor WMI padrão que define classes que modelam o [*IPMI*](windows-remote-management-glossary.md) e seus dados. O [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) é uma DLL com que obtém dados do BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Consulte [*estilo do controlador de teclado (KCS)*](windows-remote-management-glossary.md).

</dd> <dt>

**Autenticação Kerberos**
</dt> <dd>

Um método de autenticação mútua entre o cliente e o servidor que usa chaves criptografadas. Para computadores em execução em um sistema operacional baseado no Windows, a conta do cliente deve ser uma conta de domínio no mesmo domínio que o servidor. Quando um cliente usa credenciais padrão, o Kerberos é o método de autenticação se a cadeia de conexão não for uma das seguintes: localhost, 127.0.0.1 ou \[ :: 1 \] .

</dd> <dt>

**Estilo do controlador de teclado (KCS)**
</dt> <dd>

O protocolo usado pelo [*driver IPMI*](windows-remote-management-glossary.md) para se comunicar com o [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Um serviço de gerenciamento que implementa WS-Management protocolo para enviar e receber mensagens. O WinRM é um serviço de escuta. Um ouvinte é definido por um transporte (HTTP ou HTTPS) e um endereço IPv4 ou IPv6. Você pode criar mais de uma instância de ouvinte do WinRM em um único computador fornecendo a eles um número de porta ou endereço TCP/IP diferente.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Um pacote de informações transmitidas entre computadores ou redes separadas construídas com o protocolo [*SOAP*](windows-remote-management-glossary.md) . O pacote tem um cabeçalho, que descreve o destino e o transporte da mensagem e um corpo que contém o conteúdo a ser usado quando a mensagem chega. Uma mensagem é uma combinação de elementos de especificações como [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Um namespace do [*WMI*](windows-remote-management-glossary.md) , que é um agrupamento lógico de classes e instâncias do WMI para controlar o escopo e o acesso. A fonte de dados de gerenciamento mais frequente para sistemas que executam o Windows é o \\ namespace raiz cimv2, que contém classes como o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process). Os namespaces aparecem no URI de recurso para classes WMI, por exemplo https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .

</dd> <dt>

**Negociar autenticação**
</dt> <dd>

Um tipo de autenticação negociado e de logon único que é a implementação do Windows do [*mecanismo de negociação de GSSAPI simples e protegido (SPNEGO)*](windows-remote-management-glossary.md). A negociação SPNEGO determina se a autenticação é manipulada por Kerberos ou NTLM. Kerberos é o mecanismo preferencial. A autenticação de negociação em sistemas baseados no Windows também é chamada de autenticação integrada do Windows.

</dd> <dt>

**sensor numérico**
</dt> <dd>

Um tipo numérico de sensor em um [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md), por exemplo, temperatura ou voltagem.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**opção**
</dt> <dd>

Os dados adicionais exigidos pelo provedor de recursos para processar uma solicitação. Por exemplo, alguns provedores WMI exigem dados adicionais fornecidos como objetos [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) . O suporte à opção é encontrado no objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**fora de banda**
</dt> <dd>

O aplicativo cliente obtém dados diretamente do [*BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) de outro computador, em vez do [*ouvinte*](windows-remote-management-glossary.md) do WinRM no sistema operacional.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**recebimento**
</dt> <dd>

Uma mensagem de pull de [*WS-Enumeration*](windows-remote-management-glossary.md) é enviada para continuar uma enumeração iniciada por uma chamada inicial para WS-Enumeration: Enumerate. A operação pull no serviço WinRM é executada por [**enumerador. ReadItem**](enumerator-readitem.md) ou [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**Kit**
</dt> <dd>

Um [*ponto de extremidade*](windows-remote-management-glossary.md) que representa um tipo distinto de operação de gerenciamento ou valor. Um serviço expõe um ou mais recursos e alguns recursos podem ter mais de uma instância. Um recurso de gerenciamento é semelhante a uma classe WMI ou a uma tabela de banco de dados, e uma instância é semelhante a uma instância da classe ou uma linha na tabela. Por exemplo, a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa um recurso. `Win32_LogicalDisk="C:\"` é uma instância específica do recurso.

</dd> <dt>

**URI de recurso**
</dt> <dd>

O [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) usado para identificar um tipo específico de recurso, como discos ou processos, em um sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**REPOSITÓRIO**
</dt> <dd>

Consulte [*log de eventos do sistema (SEL)*](windows-remote-management-glossary.md).

</dd> <dt>

**Adaptador SEL**
</dt> <dd>

O adaptador que envia dados do [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) para o [*coletor de eventos*](windows-remote-management-glossary.md).

</dd> <dt>

**seletor**
</dt> <dd>

Um par de nome e valor que representa uma instância específica de um [*recurso*](windows-remote-management-glossary.md). Esse é essencialmente um filtro ou "chave" que identifica a instância desejada do recurso. O suporte ao seletor é encontrado no objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**sensores**
</dt> <dd>

Um dispositivo de medição em um [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> <dt>

**serviço**
</dt> <dd>

Um aplicativo que fornece serviços de gerenciamento para clientes por meio do protocolo WS-Management e outros [*Serviços Web*](windows-remote-management-glossary.md). Um serviço é geralmente o mesmo que o [*ouvinte*](windows-remote-management-glossary.md) em uma rede. O serviço tem um endereço de transporte físico.

</dd> <dt>

**sessão**
</dt> <dd>

Uma conexão entre um [*cliente*](windows-remote-management-glossary.md) gerenciamento remoto do Windows e o [*ouvinte*](windows-remote-management-glossary.md)ou serviço do WinRM local ou remoto. Essa conexão é semelhante à conexão entre um script de cliente WMI e o WMI em um servidor remoto. As operações de sessão, como a enumeração de um recurso (enumerar), a obtenção de uma instância de um recurso (Get) ou a execução de um método de recurso (Invoke) são métodos do objeto de **sessão** . Um objeto de **sessão** é criado por [**WSMan. CreateSession**](wsman-createsession.md).

</dd> <dt>

**Mecanismo de negociação GSS-API simples e protegido (SPNEGO)**
</dt> <dd>

Um mecanismo de autenticação usado pelo cliente ou servidor que recebe solicitações de dados por meio do WinRM em um contexto de Active Directory. O SPNEGO é baseado em um protocolo RFC (solicitação de comentários) produzido pela IETF (Internet Engineering Task Force). O SPNEGO também é conhecido como [*autenticação integrada do Windows*](windows-remote-management-glossary.md), o termo usado na gerenciamento remoto do Windows tópicos da ajuda.

</dd> <dt>

**SOAP (Protocolo Simples de Acesso a Objetos)**
</dt> <dd>

Um protocolo baseado em XML usado pelos serviços Web.

</dd> <dt>

**SOAP**
</dt> <dd>

Consulte [*protocolo SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md).

</dd> <dt>

**SPNEGO**
</dt> <dd>

Consulte [*mecanismo de negociação GSS-API simples e protegido (SPNEGO)*](windows-remote-management-glossary.md).

</dd> <dt>

**Registro de eventos do sistema (SEL)**
</dt> <dd>

O banco de dados de eventos no hardware do [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) . O [*adaptador SEL*](windows-remote-management-glossary.md) transmite esses eventos para o sistema operacional.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**URI (Uniform Resource Identifier)**
</dt> <dd>

Uma cadeia de caracteres que identifica um recurso na empresa, como um computador, um processo, uma unidade de disco ou um sensor de temperatura em um [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md). O URI é o mecanismo de endereçamento do serviço Web definido na IETF (Internet Engineering Task Force) Uniform Resource Identifier (URI): sintaxe genérica \[ RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Consulte [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**serviço Web**
</dt> <dd>

Um aplicativo de software usado para interação entre computadores na Internet ou em uma rede. Os serviços Web são descritos pelo [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md). A descrição específica do serviço Web informa outros serviços como interagir com o serviço Web usando mensagens SOAP. As mensagens são transmitidas entre computadores por um transporte, geralmente HTTP ou HTTPS. O [*WS-Addressing*](windows-remote-management-glossary.md), o [*WS-Eventing*](windows-remote-management-glossary.md)e o [*WS-Management*](windows-remote-management-glossary.md) são exemplos de protocolos usados por aplicativos de serviço Web para se comunicar entre si.

</dd> <dt>

**WSDL (Web Service Description Language)**
</dt> <dd>

Uma linguagem baseada em XML usada para definir como interagir com um serviço Web. Normalmente, o WSDL descreve quais mensagens SOAP o serviço Web requer para retornar dados ou executar operações. O WSDL permite que uma implementação de um sistema operacional se comunique com o serviço Web implementado em outro sistema operacional, desde que os requisitos do WSDL sejam atendidos.

</dd> <dt>

**Autenticação Integrada do Windows**
</dt> <dd>

Consulte [*negociar autenticação*](windows-remote-management-glossary.md).

</dd> <dt>

**WMI (Instrumentação de Gerenciamento do Windows)**
</dt> <dd>

A implementação da Microsoft do padrão Web-Based Enterprise Management (WBEM) publicado pela [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md). O WMI permite que você gerencie computadores locais e remotos e os modelos de computador e rede usando uma extensão do padrão de [*modelo CIM (CIM)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Gerenciamento Remoto do Windows (WinRM)**
</dt> <dd>

A implementação da Microsoft de um serviço Web de gerenciamento com base no protocolo [*WS-Management*](windows-remote-management-glossary.md) padrão público.

</dd> <dt>

**Shell remoto do Windows (WinRS)**
</dt> <dd>

Uma ferramenta de shell que se baseia em [*gerenciamento remoto do Windows*](windows-remote-management-glossary.md) executar comandos remotos, especialmente para servidores sem periféricos. A ferramenta de linha de comando é winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Consulte [*Instrumentação de gerenciamento do Windows (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Plug-in WMI**
</dt> <dd>

O plug-in do WinRM que disponibiliza dados do WMI para clientes WinRM.

</dd> <dt>

**WS-Addressing (WSA)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, que cria um sistema de endereçamento usado nos cabeçalhos de mensagens enviadas pela Internet. O padrão define como os recursos podem ser localizados em redes e firewalls. WS-Addressing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para enumerar uma sequência de elementos XML que pode representar coleções de dados, logs ou outras estruturas de informações lineares. WS-Enumeration é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, que permite que um serviço Web (o assinante) assine e aceite mensagens de notificação de eventos de outro serviço Web (a origem do evento). WS-Eventing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Management**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para compartilhar dados de gerenciamento entre todos os sistemas operacionais, computadores e dispositivos. Todas as [*mensagens*](windows-remote-management-glossary.md) enviadas pelo cliente ou pelos componentes do servidor WinRM usam esse protocolo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para acessar representações XML de recursos baseados em serviços da Web por meio de um conjunto simples de verbos, como Get, put, Invoke ou Delete. WS-Transfer define as operações para enviar e receber a representação de um recurso específico e operações para criar ou excluir um recurso e sua representação correspondente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Uma notação de caminho para endereçar partes de um documento XML, semelhante a uma URL. Uma expressão XPath é uma sequência de frases a serem obtidas do local atual no documento XML para outro nó ou conjunto de nós. As frases são separadas por caracteres de barra ("/"). O serviço WinRM dá suporte a [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) para [*dialeto de fragmento*](windows-remote-management-glossary.md).

</dd> </dl>

 

 